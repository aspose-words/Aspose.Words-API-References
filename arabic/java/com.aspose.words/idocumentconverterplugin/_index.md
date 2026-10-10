---
title: "IDocumentConverterPlugin"
linktitle: "IDocumentConverterPlugin"
second_title: "Aspose.Words لـ Java"
description: "يعرّف واجهة لمكوّن تحويل خارجي في Java."
type: docs
weight: 757
url: /ar/java/com.aspose.words/idocumentconverterplugin/
---
```
public interface IDocumentConverterPlugin
```

يحدد واجهة لمكوّن تحويل خارجي.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions) | يحوّل الصفحات من المستند من تدفق الإدخال إلى مصفوفة من الصور. |
### convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions}
```
public abstract OutputStream[] convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)
```


يحوّل الصفحات من المستند من تدفق الإدخال إلى مصفوفة من الصور.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق الإدخال. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | خيارات تحميل المستند. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | خيارات الحفظ. |

**Returns:**
java.io.OutputStream[] - مصفوفة من تدفقات صور الصفحات.
