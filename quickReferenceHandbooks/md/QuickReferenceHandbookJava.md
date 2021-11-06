# QUICK REFERENCE HANDBOOK JAVA

## ENCODING

### DIACRITICS / SPECIAL CHARACTERS NOT PROCESSED CORRECTLY

- [ ] STOP APPLICATION IF NECESSARY
- [ ] CHECK CHARSET (SEE "CHECK CHARSET" below)
- [ ] SET ENCODING PROPERTY IN START SCRIPT (UTF-8, ...)

    ```
    -Dfile.encoding=UTF-8
    ```
- [ ] START APPLICATION

### TEST CASES FAIL BECAUSE DIACRITICS / SPECIAL CHARACTERS NOT PROCESSED CORRECTLY

- [ ] CHECK CHARSET (SEE "CHECK CHARSET" below)
- [ ] OPEN BUILD FILE (build.gradle)
- [ ] SET ENCODING IN BUILD FILE (UTF-8, ...)

    ```
    compileJava.options.encoding = 'UTF-8'
    compileTestJava.options.encoding = 'UTF-8'
    ```

### CHECK CHARSET

- [ ] COMPILE AND RUN PROGRAM

```
import java.nio.charset.Charset;

public class CharsetCheck {
    public static void main(String args[]) {
        System.out.println(Charset.defaultCharset().displayName());
    }
}
```