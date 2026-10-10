---
title: "IDocumentProcessorPlugin"
linktitle: "IDocumentProcessorPlugin"
second_title: "Aspose.Words لـ Java"
description: "يحدد واجهة لمكوّن إضافي لمعالج المستندات الخارجي في Java."
type: docs
weight: 761
url: /ar/java/com.aspose.words/idocumentprocessorplugin/
---
```
public interface IDocumentProcessorPlugin
```

يحدد واجهة لمكوّن معالجة مستندات خارجي.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [append(InputStream inputStream, LoadOptions loadOptions)](#append-java.io.InputStream-com.aspose.words.LoadOptions) | أضف المستند بتحميله باستخدام خيارات التحميل المحددة. |
| [load(InputStream inputStream, LoadOptions loadOptions)](#load-java.io.InputStream-com.aspose.words.LoadOptions) | حمّل المستند باستخدام خيارات التحميل المحددة. |
| [save(OutputStream outputStream, SaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)](#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | يضيف علامة مائية صورة على كل صفحة من المستند الذي تم تحميله بواسطة طريقة [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions). |
| [setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)](#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions) | يضيف علامة مائية نصية على كل صفحة من المستند الذي تم تحميله بواسطة طريقة [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions). |
| [toDocument()](#toDocument) | يحلل المستند الذي تم تحميله بواسطة طريقة [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) إلى كائن [Document](../../com.aspose.words/document/). |
| [toPages(FixedPageSaveOptions saveOptions)](#toPages-com.aspose.words.FixedPageSaveOptions) | يحفظ كل صفحة من المستند الذي تم تحميله بواسطة طريقة [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) باستخدام خيارات حفظ الصفحة الثابتة المحددة. |
### append(InputStream inputStream, LoadOptions loadOptions) {#append-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void append(InputStream inputStream, LoadOptions loadOptions)
```


أضف المستند بتحميله باستخدام خيارات التحميل المحددة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق الإدخال. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | خيارات تحميل المستند. يمكن أن تكون null، وفي هذه الحالة يتم تحميل المستند باستخدام خيارات التحميل الافتراضية. |

### load(InputStream inputStream, LoadOptions loadOptions) {#load-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void load(InputStream inputStream, LoadOptions loadOptions)
```


حمّل المستند باستخدام خيارات التحميل المحددة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| inputStream | java.io.InputStream | دفق الإدخال. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | خيارات تحميل المستند. يمكن أن تكون null، وفي هذه الحالة يتم تحميل المستند باستخدام خيارات التحميل الافتراضية. |

### save(OutputStream outputStream, SaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void save(OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions) {#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public abstract void setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)
```


يضيف علامة مائية صورة على كل صفحة من المستند الذي تم تحميله بواسطة طريقة [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageWatermark | java.io.InputStream | الصورة المستخدمة كعلامة مائية. |
| imageWatermarkOptions | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | خيارات علامة مائية للصورة. |

### setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions) {#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public abstract void setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)
```


يضيف علامة مائية نصية على كل صفحة من المستند الذي تم تحميله بواسطة طريقة [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| textWatermark | java.lang.String | النص المستخدم كعلامة مائية. |
| textWatermarkOptions | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | خيارات علامة مائية للنص. |

### toDocument() {#toDocument}
```
public abstract Document toDocument()
```


يحلل المستند الذي تم تحميله بواسطة طريقة [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) إلى كائن [Document](../../com.aspose.words/document/).

**Returns:**
[Document](../../com.aspose.words/document/)
### toPages(FixedPageSaveOptions saveOptions) {#toPages-com.aspose.words.FixedPageSaveOptions}
```
public abstract OutputStream[] toPages(FixedPageSaveOptions saveOptions)
```


يحفظ كل صفحة من المستند الذي تم تحميله بواسطة طريقة [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) باستخدام خيارات حفظ الصفحة الثابتة المحددة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| saveOptions | [FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions/) |  |

**Returns:**
java.io.OutputStream[]
