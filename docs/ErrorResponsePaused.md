

# ErrorResponsePaused

## anyOf schemas
* [Boolean](Boolean.md)
* [ErrorResponsePausedAnyOf](ErrorResponsePausedAnyOf.md)

## Example
```java
// Import classes:
import io.planpoint.model.ErrorResponsePaused;
import io.planpoint.model.Boolean;
import io.planpoint.model.ErrorResponsePausedAnyOf;

public class Example {
    public static void main(String[] args) {
        ErrorResponsePaused exampleErrorResponsePaused = new ErrorResponsePaused();

        // create a new Boolean
        Boolean exampleBoolean = new Boolean();
        // set ErrorResponsePaused to Boolean
        exampleErrorResponsePaused.setActualInstance(exampleBoolean);
        // to get back the Boolean set earlier
        Boolean testBoolean = (Boolean) exampleErrorResponsePaused.getActualInstance();

        // create a new ErrorResponsePausedAnyOf
        ErrorResponsePausedAnyOf exampleErrorResponsePausedAnyOf = new ErrorResponsePausedAnyOf();
        // set ErrorResponsePaused to ErrorResponsePausedAnyOf
        exampleErrorResponsePaused.setActualInstance(exampleErrorResponsePausedAnyOf);
        // to get back the ErrorResponsePausedAnyOf set earlier
        ErrorResponsePausedAnyOf testErrorResponsePausedAnyOf = (ErrorResponsePausedAnyOf) exampleErrorResponsePaused.getActualInstance();
    }
}
```


