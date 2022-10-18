---
title: FieldFileSize
second_title: Aspose.Words for Java API Reference
description: Implements the FILESIZE field.
type: docs
weight: 188
url: /java/com.aspose.words/fieldfilesize/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldFileSize extends Field
```

Implements the FILESIZE field.

To learn more, visit the **Working with Fields** documentation article.

Retrieves the size of the current document's file or 0 if the size cannot be determined.

In the current implementation, uses the [Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--) property to retrieve the file name used to determine the file size.
## Methods

| Method | Description |
| --- | --- |
| [isInKilobytes()](#isInKilobytes--) | Gets whether to display the file size in kilobytes. |
| [isInKilobytes(boolean value)](#isInKilobytes-boolean-) | Sets whether to display the file size in kilobytes. |
| [isInMegabytes()](#isInMegabytes--) | Gets whether to display the file size in megabytes. |
| [isInMegabytes(boolean value)](#isInMegabytes-boolean-) | Sets whether to display the file size in megabytes. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
### isInKilobytes() {#isInKilobytes--}
```
public boolean isInKilobytes()
```


Gets whether to display the file size in kilobytes.

**Returns:**
boolean - Whether to display the file size in kilobytes.
### isInKilobytes(boolean value) {#isInKilobytes-boolean-}
```
public void isInKilobytes(boolean value)
```


Sets whether to display the file size in kilobytes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to display the file size in kilobytes. |

### isInMegabytes() {#isInMegabytes--}
```
public boolean isInMegabytes()
```


Gets whether to display the file size in megabytes.

**Returns:**
boolean - Whether to display the file size in megabytes.
### isInMegabytes(boolean value) {#isInMegabytes-boolean-}
```
public void isInMegabytes(boolean value)
```


Sets whether to display the file size in megabytes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to display the file size in megabytes. |

### getSwitchType(String switchName) {#getSwitchType-java.lang.String-}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
