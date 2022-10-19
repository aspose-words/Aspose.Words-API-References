---
title: FieldFileName
second_title: Aspose.Words for Java API Reference
description: Implements the FILENAME field.
type: docs
weight: 187
url: /java/com.aspose.words/fieldfilename/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldFileName extends Field
```

Implements the FILENAME field.

To learn more, visit the **Working with Fields** documentation article.

Retrieves the name of the current document from its storage location.

In the current implementation, uses the [Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--) property to retrieve the file name. If the document was loaded from a stream or created blank, uses the name of the file that is being saved to (if known).
## Methods

| Method | Description |
| --- | --- |
| [getIncludeFullPath()](#getIncludeFullPath--) | Gets whether to include the full file path name. |
| [setIncludeFullPath(boolean value)](#setIncludeFullPath-boolean-) | Sets whether to include the full file path name. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
### getIncludeFullPath() {#getIncludeFullPath--}
```
public boolean getIncludeFullPath()
```


Gets whether to include the full file path name.

**Returns:**
boolean - Whether to include the full file path name.
### setIncludeFullPath(boolean value) {#setIncludeFullPath-boolean-}
```
public void setIncludeFullPath(boolean value)
```


Sets whether to include the full file path name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to include the full file path name. |

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
