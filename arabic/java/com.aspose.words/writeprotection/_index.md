---
title: "WriteProtection"
linktitle: "WriteProtection"
second_title: "Aspose.Words لـ Java"
description: "يحدد إعدادات الحماية من الكتابة لمستند في Java."
type: docs
weight: 738
url: /ar/java/com.aspose.words/writeprotection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class WriteProtection implements Cloneable
```

يحدد إعدادات الحماية من الكتابة للمستند.

لمزيد من المعلومات، قم بزيارة مقالة الوثائق [ Protect or Encrypt a Document ][Protect or Encrypt a Document]

 **Remarks:** 

تحدد حماية الكتابة ما إذا كان المؤلف قد أوصى بفتح المستند للقراءة فقط و/أو يتطلب كلمة مرور لتعديل المستند.

حماية الكتابة تختلف عن حماية المستند. يتم تحديد حماية الكتابة في Microsoft Word في خيارات مربع حوار حفظ باسم.

لا تقوم بإنشاء مثيلات من هذه الفئة مباشرة. يمكنك الوصول إلى إعدادات حماية المستند عبر الخاصية [Document.getWriteProtection()](../../com.aspose.words/document/\#getWriteProtection).

 **Examples:** 

يوضح كيفية حماية مستند باستخدام كلمة مرور.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```


[Protect or Encrypt a Document]: https://docs.aspose.com/words/java/protect-or-encrypt-a-document/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getReadOnlyRecommended()](#getReadOnlyRecommended) | يحدد ما إذا كان مؤلف المستند قد أوصى بفتح المستند للقراءة فقط. |
| [isWriteProtected()](#isWriteProtected) | يرجع  true  عندما يتم تعيين كلمة مرور حماية الكتابة. |
| [setPassword(String password)](#setPassword-java.lang.String) | يضبط كلمة مرور حماية الكتابة للمستند. |
| [setReadOnlyRecommended(boolean value)](#setReadOnlyRecommended-boolean) | يحدد ما إذا كان مؤلف المستند قد أوصى بفتح المستند للقراءة فقط. |
| [validatePassword(String password)](#validatePassword-java.lang.String) | يرجع  true  إذا كانت كلمة المرور المحددة هي نفسها كلمة مرور حماية الكتابة التي تم حماية المستند بها. |
### getReadOnlyRecommended() {#getReadOnlyRecommended}
```
public boolean getReadOnlyRecommended()
```


يحدد ما إذا كان مؤلف المستند قد أوصى بفتح المستند للقراءة فقط.

 **Examples:** 

يوضح كيفية حماية مستند باستخدام كلمة مرور.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### isWriteProtected() {#isWriteProtected}
```
public boolean isWriteProtected()
```


يرجع  true  عندما يتم تعيين كلمة مرور حماية الكتابة.

 **Examples:** 

يوضح كيفية حماية مستند باستخدام كلمة مرور.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Returns:**
منطقي -  true  عندما يتم تعيين كلمة مرور حماية الكتابة.
### setPassword(String password) {#setPassword-java.lang.String}
```
public void setPassword(String password)
```


يضبط كلمة مرور حماية الكتابة للمستند.

 **Remarks:** 

إذا تم تعيين كلمة مرور، سيطلب Microsoft Word من المستخدم إدخالها أو فتح المستند للقراءة فقط.

 **Examples:** 

يوضح كيفية حماية مستند باستخدام كلمة مرور.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| كلمة مرور | java.lang.String | كلمة المرور التي سيتم تعيينها. لا يمكن أن تكون  null ، ولكن يمكن أن تكون سلسلة فارغة. |

### setReadOnlyRecommended(boolean value) {#setReadOnlyRecommended-boolean}
```
public void setReadOnlyRecommended(boolean value)
```


يحدد ما إذا كان مؤلف المستند قد أوصى بفتح المستند للقراءة فقط.

 **Examples:** 

يوضح كيفية حماية مستند باستخدام كلمة مرور.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### validatePassword(String password) {#validatePassword-java.lang.String}
```
public boolean validatePassword(String password)
```


يرجع  true  إذا كانت كلمة المرور المحددة هي نفسها كلمة مرور حماية الكتابة التي تم حماية المستند بها. إذا لم يكن المستند محمياً بحماية كتابة باستخدام كلمة مرور فسيُرجع  false .

 **Examples:** 

يوضح كيفية حماية مستند باستخدام كلمة مرور.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| كلمة مرور | java.lang.String |  |

**Returns:**
boolean
