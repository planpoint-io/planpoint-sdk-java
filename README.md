# planpoint-sdk-java

Official Java SDK for the [Planpoint](https://app.planpoint.io) API.

## Requirements

- Java 17+
- Maven or Gradle

> **Windows Note:** Make sure `JAVA_HOME` is set before running Maven:
>
> ```powershell
> $env:JAVA_HOME = "C:\Program Files\Microsoft\jdk-17.0.18.8-hotspot"
> $env:Path += ";$env:JAVA_HOME\bin"
> ```

## Installation

The SDK is served via [JitPack](https://jitpack.io) — no auth or registry setup required.

### Maven

```xml
<repositories>
  <repository>
    <id>jitpack.io</id>
    <url>https://jitpack.io</url>
  </repository>
</repositories>

<dependencies>
  <dependency>
    <groupId>com.github.planpoint-io</groupId>
    <artifactId>planpoint-sdk-java</artifactId>
    <version>main-SNAPSHOT</version>
  </dependency>
</dependencies>

<build>
  <plugins>
    <plugin>
      <groupId>org.codehaus.mojo</groupId>
      <artifactId>exec-maven-plugin</artifactId>
      <version>3.1.0</version>
      <configuration>
        <mainClass>com.yourpackage.Main</mainClass>
      </configuration>
    </plugin>
  </plugins>
</build>
```

### Gradle

```groovy
repositories {
    maven { url 'https://jitpack.io' }
}

dependencies {
    implementation 'com.github.planpoint-io:planpoint-sdk-java:main-SNAPSHOT'
}
```

## Quick Start

```java
import io.planpoint.ApiClient;
import io.planpoint.api.AuthenticationApi;
import io.planpoint.api.ProjectsApi;
import io.planpoint.model.LoginBody;
import io.planpoint.model.AuthResponse;
import io.planpoint.model.ProjectSummary;

import java.util.List;

public class Main {
    static ApiClient makeClient(String token) {
        ApiClient client = new ApiClient();
        client.setScheme("https");
        client.setHost("app.planpoint.io");
        client.setPort(-1);
        if (!token.isEmpty()) {
            client.setRequestInterceptor(req -> req.header("Authorization", "Bearer " + token));
        }
        return client;
    }

    public static void main(String[] args) throws Exception {
        // 1. Authenticate
        LoginBody loginBody = new LoginBody();
        loginBody.setUsername("you@example.com");
        loginBody.setPassword("yourpassword");
        AuthResponse auth = new AuthenticationApi(makeClient("")).login(loginBody);
        String token = auth.getAccessToken();

        // 2. Fetch your projects using authenticated client
        List<ProjectSummary> projects = new ProjectsApi(makeClient(token)).getMyProjects();
        for (ProjectSummary p : projects) {
            System.out.println(p.getName());
        }
    }
}
```

## API Reference

### Authentication

#### `new AuthenticationApi(client).login(LoginBody body)`

Authenticate and receive a JWT token.

| Field         | Type      | Required | Description              |
| ------------- | --------- | -------- | ------------------------ |
| `username`    | `String`  | Yes      | User email               |
| `password`    | `String`  | No       | User password            |
| `impersonate` | `Boolean` | No       | Impersonate another user |

**Returns:** `AuthResponse` — `.getAccessToken(): String`

---

### Projects

#### `new ProjectsApi(client).getMyProjects()`

List all projects belonging to the authenticated user. Requires auth.

**Returns:** `List<ProjectSummary>` — `.getName()`, `.getNamespace()`, `.getHostName()`, `.getStatus()`, `.getPaused()`, `.getCreatedAt()`

---

#### `new ProjectsApi(client).findProject(FindProjectBody body)`

Find a public project by namespace and hostname. No auth required.

| Field       | Type     | Required | Description       |
| ----------- | -------- | -------- | ----------------- |
| `namespace` | `String` | Yes      | Project namespace |
| `hostName`  | `String` | Yes      | Allowed hostname  |

**Returns:** `Project`

---

#### `new ProjectsApi(client).getProject(String id)`

Get a project by ID. Requires auth.

**Returns:** `Project`

---

#### `new ProjectsApi(client).updateProject(String id, Object body)`

Update project settings. Requires auth.

**Returns:** `Project`

---

### Groups

#### `new GroupsApi(client).getGroups()`

List all groups for the authenticated user. Requires auth.

**Returns:** `GroupsListResponse` — `.getRecords(): List<Group>`, `.getCount(): Integer`

---

#### `new GroupsApi(client).getGroup(String id)`

Get a group by ID. Requires auth.

**Returns:** `Group` — `.getName()`, `.getNamespace()`, `.getHostName()`, `.getType()`

---

#### `new GroupsApi(client).createGroup(CreateGroupBody body)`

Create a new group. Requires auth.

**Returns:** `Group`

---

#### `new GroupsApi(client).updateGroup(String id, Object body)`

Update a group. Requires auth.

**Returns:** `Group`

---

### Floors

#### `new FloorsApi(client).getFloors(String pid)`

List all floors for a project. Requires auth.

| Param | Type     | Required | Description      |
| ----- | -------- | -------- | ---------------- |
| `pid` | `String` | Yes      | Project ObjectId |

**Returns:** `List<FloorFull>` — `.getName()`, `.getProject()`, `.getLevel()`, `.getPosition()`, `.getPath()`

---

#### `new FloorsApi(client).getFloor(String id)`

Get a floor by ID. Requires auth.

**Returns:** `FloorFull`

---

#### `new FloorsApi(client).createFloor(CreateFloorBody body)`

Create a new floor. Requires auth.

**Returns:** `FloorFull`

---

#### `new FloorsApi(client).updateFloor(String id, Object body)`

Update a floor. Requires auth.

**Returns:** `FloorFull`

---

### Units

#### `new UnitsApi(client).getUnits(String pid)`

List all units for a project. Requires auth.

| Param | Type     | Required | Description      |
| ----- | -------- | -------- | ---------------- |
| `pid` | `String` | Yes      | Project ObjectId |

**Returns:** `UnitsListResponse` — `.getRecords(): List<UnitFull>`, `.getCount(): Integer`

`UnitFull` fields: `.getFloor()`, `.getName()`, `.getUnitNumber()`, `.getStatus()`, `.getPrice()`, `.getBed()`, `.getBath()`, `.getSqft()`, `.getModel()`

`status` values: `Available` | `OnHold` | `Sold` | `Leased` | `Unavailable`

---

#### `new UnitsApi(client).getUnit(String id)`

Get a unit by ID. Requires auth.

**Returns:** `UnitFull`

---

#### `new UnitsApi(client).createUnit(CreateUnitBody body)`

Create a new unit. Requires auth.

**Returns:** `UnitFull`

---

#### `new UnitsApi(client).updateUnit(String id, Object body)`

Update a unit. Requires auth.

**Returns:** `UnitFull`

---

#### `new UnitsApi(client).deleteUnit(String id)`

Delete a unit. Requires auth.

---

#### `new UnitsApi(client).batchUpdateUnits(BatchUpdateUnitsBody body)`

Update multiple units at once. Requires auth.

| Field       | Type           | Required | Description              |
| ----------- | -------------- | -------- | ------------------------ |
| `ids`       | `List<String>` | Yes      | Unit ObjectIds to update |
| `patchData` | `Object`       | Yes      | Fields to apply to all   |

**Returns:** `List<UnitFull>`

---

### Leads

#### `new LeadsApi(client).getLeads(String pid)`

List all leads for a project. Requires auth.

| Param | Type     | Required | Description      |
| ----- | -------- | -------- | ---------------- |
| `pid` | `String` | Yes      | Project ObjectId |

**Returns:** `List<Lead>` — `.getName()`, `.getEmail()`, `.getPhone()`, `.getMessage()`, `.getUnit()`, `.getCreatedAt()`

---

## Links

- **[Install via JitPack (Maven/Gradle)](https://jitpack.io/#planpoint-io/planpoint-sdk-java)**
- [Java SDK on GitHub](https://github.com/planpoint-io/planpoint-sdk-java)
- [Planpoint App](https://app.planpoint.io)
- [TypeScript SDK on npm](https://www.npmjs.com/package/@planpoint/sdk)
- [Python SDK on PyPI](https://pypi.org/project/planpoint-sdk)
- [Go SDK on GitHub](https://github.com/planpoint-io/planpoint-sdk-go)
- [PHP SDK on GitHub](https://github.com/planpoint-io/planpoint-sdk-php)
