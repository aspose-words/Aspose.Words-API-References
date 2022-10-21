---
title: ChmLoadOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify additional options when loading CHM document into a  object.
type: docs
weight: 72
url: /java/com.aspose.words/chmloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions)
```
public class ChmLoadOptions extends LoadOptions
```

Allows to specify additional options when loading CHM document into a [Document](../../com.aspose.words/document) object.

To learn more, visit the **Specify Load Options** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [ChmLoadOptions()](#ChmLoadOptions--) | Initializes a new instance of this class with default values. |
## Methods

| Method | Description |
| --- | --- |
| [getOriginalFileName()](#getOriginalFileName--) | The name of the CHM file. |
| [setOriginalFileName(String value)](#setOriginalFileName-java.lang.String-) | The name of the CHM file. |
### ChmLoadOptions() {#ChmLoadOptions--}
```
public ChmLoadOptions()
```


Initializes a new instance of this class with default values.

### getOriginalFileName() {#getOriginalFileName--}
```
public String getOriginalFileName()
```


The name of the CHM file. Default value is  null .

CHM documents may contain links that reference the same document by file name. Aspose.Words supports such links and normally uses [Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--) to check whether the file referenced by a link is the file that is being loaded. If a document is loaded from a stream, its original file name should be specified explicitly via this property, since it cannot be determined automatically.

If a CHM document is loaded from a file and a non-null value for this property is specified, the value will take priority over the actual name of the file stored in [Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--).

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setOriginalFileName(String value) {#setOriginalFileName-java.lang.String-}
```
public void setOriginalFileName(String value)
```


The name of the CHM file. Default value is  null .

CHM documents may contain links that reference the same document by file name. Aspose.Words supports such links and normally uses [Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--) to check whether the file referenced by a link is the file that is being loaded. If a document is loaded from a stream, its original file name should be specified explicitly via this property, since it cannot be determined automatically.

If a CHM document is loaded from a file and a non-null value for this property is specified, the value will take priority over the actual name of the file stored in [Document.getOriginalFileName()](../../com.aspose.words/document\#getOriginalFileName--).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

