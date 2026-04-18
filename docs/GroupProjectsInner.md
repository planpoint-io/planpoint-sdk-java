

# GroupProjectsInner

## anyOf schemas
* [GroupProject](GroupProject.md)
* [String](String.md)

## Example
```java
// Import classes:
import io.planpoint.model.GroupProjectsInner;
import io.planpoint.model.GroupProject;
import io.planpoint.model.String;

public class Example {
    public static void main(String[] args) {
        GroupProjectsInner exampleGroupProjectsInner = new GroupProjectsInner();

        // create a new GroupProject
        GroupProject exampleGroupProject = new GroupProject();
        // set GroupProjectsInner to GroupProject
        exampleGroupProjectsInner.setActualInstance(exampleGroupProject);
        // to get back the GroupProject set earlier
        GroupProject testGroupProject = (GroupProject) exampleGroupProjectsInner.getActualInstance();

        // create a new String
        String exampleString = new String();
        // set GroupProjectsInner to String
        exampleGroupProjectsInner.setActualInstance(exampleString);
        // to get back the String set earlier
        String testString = (String) exampleGroupProjectsInner.getActualInstance();
    }
}
```


