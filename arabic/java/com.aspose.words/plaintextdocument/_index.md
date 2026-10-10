---
title: "PlainTextDocument"
linktitle: "PlainTextDocument"
second_title: "Aspose.Words لـ Java"
description: "يسمح باستخراج تمثيل النص العادي لمحتوى المستند في Java."
type: docs
weight: 549
url: /ar/java/com.aspose.words/plaintextdocument/
---

**Inheritance:**
java.lang.Object
```
public class PlainTextDocument
```

يسمح باستخراج تمثيل النص العادي لمحتوى المستند.

لمزيد من المعلومات، قم بزيارة مقالة الوثائق [ Working with Text Document ][Working with Text Document].

 **Examples:** 

يعرض كيفية تحميل محتويات مستند Microsoft Word كنص عادي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PlainTextDocument.Load.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.Load.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 
```


[Working with Text Document]: https://docs.aspose.com/words/java/working-with-text-document/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [PlainTextDocument(String fileName)](#PlainTextDocument-java.lang.String) | ينشئ مستند نص عادي من ملف. |
| [PlainTextDocument(String fileName, LoadOptions loadOptions)](#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions) | ينشئ مستند نص عادي من ملف. |
| [PlainTextDocument(InputStream stream)](#PlainTextDocument-java.io.InputStream) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
| [PlainTextDocument(InputStream stream, LoadOptions loadOptions)](#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties) | يحصل على [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) للمستند. |
| [getCustomDocumentProperties()](#getCustomDocumentProperties) | يحصل على [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) للمستند. |
| [getText()](#getText) | يحصل على المحتوى النصي للمستند مدموجًا كسلسلة. |
### PlainTextDocument(String fileName) {#PlainTextDocument-java.lang.String}
```
public PlainTextDocument(String fileName)
```


ينشئ مستند نص عادي من ملف. يكتشف تنسيق الملف تلقائيًا.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | اسم الملف لاستخراج النص منه. |

### PlainTextDocument(String fileName, LoadOptions loadOptions) {#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions}
```
public PlainTextDocument(String fileName, LoadOptions loadOptions)
```


ينشئ مستند نص عادي من ملف. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fileName | java.lang.String | اسم الملف لاستخراج النص منه. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | خيارات إضافية للاستخدام عند تحميل مستند. يمكن أن تكون null. |

### PlainTextDocument(InputStream stream) {#PlainTextDocument-java.io.InputStream}
```
public PlainTextDocument(InputStream stream)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### PlainTextDocument(InputStream stream, LoadOptions loadOptions) {#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions}
```
public PlainTextDocument(InputStream stream, LoadOptions loadOptions)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |

### getBuiltInDocumentProperties() {#getBuiltInDocumentProperties}
```
public BuiltInDocumentProperties getBuiltInDocumentProperties()
```


يحصل على [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) للمستند.

 **Examples:** 

يعرض كيفية تحميل محتويات مستند Microsoft Word كنص عادي ثم الوصول إلى الخصائص المدمجة للمستند الأصلي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");

 doc.save(getArtifactsDir() + "PlainTextDocument.BuiltInProperties.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.BuiltInProperties.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 Assert.assertEquals("John Doe", plaintext.getBuiltInDocumentProperties().getAuthor());
 
```

**Returns:**
[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties/) - [getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getBuiltInDocumentProperties) of the document.
### getCustomDocumentProperties() {#getCustomDocumentProperties}
```
public CustomDocumentProperties getCustomDocumentProperties()
```


يحصل على [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) للمستند.

 **Examples:** 

يعرض كيفية تحميل محتويات مستند Microsoft Word كنص عادي ثم الوصول إلى الخصائص المخصصة للمستند الأصلي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 doc.getCustomDocumentProperties().add("Location of writing", "123 Main St, London, UK");

 doc.save(getArtifactsDir() + "PlainTextDocument.CustomDocumentProperties.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.CustomDocumentProperties.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 Assert.assertEquals("123 Main St, London, UK", plaintext.getCustomDocumentProperties().get("Location of writing").getValue());
 
```

**Returns:**
[CustomDocumentProperties](../../com.aspose.words/customdocumentproperties/) - [getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument/\#getCustomDocumentProperties) of the document.
### getText() {#getText}
```
public String getText()
```


يحصل على المحتوى النصي للمستند مدموجًا كسلسلة.

 **Examples:** 

يعرض كيفية تحميل محتويات مستند Microsoft Word كنص عادي.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PlainTextDocument.Load.docx");

 PlainTextDocument plaintext = new PlainTextDocument(getArtifactsDir() + "PlainTextDocument.Load.docx");

 Assert.assertEquals("Hello world!", plaintext.getText().trim());
 
```

**Returns:**
java.lang.String - المحتوى النصي للمستند متسلسل كسلسلة.
