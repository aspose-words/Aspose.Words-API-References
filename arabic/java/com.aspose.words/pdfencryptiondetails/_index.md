---
title: "PdfEncryptionDetails"
linktitle: "PdfEncryptionDetails"
second_title: "Aspose.Words لـ Java"
description: "يحتوي على تفاصيل لتشفير وصلاحيات الوصول لمستند PDF في Java."
type: docs
weight: 534
url: /ar/java/com.aspose.words/pdfencryptiondetails/
---

**Inheritance:**
java.lang.Object
```
public class PdfEncryptionDetails
```

يحتوي على تفاصيل تشفير وصلاحيات الوصول لمستند PDF.

لمزيد من المعلومات، قم بزيارة مقالة الوثائق [ Protect or Encrypt a Document ][Protect or Encrypt a Document]

 **Examples:** 

يوضح كيفية تعيين الصلاحيات على مستند PDF محفوظ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```


[Protect or Encrypt a Document]: https://docs.aspose.com/words/java/protect-or-encrypt-a-document/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [PdfEncryptionDetails(String userPassword, String ownerPassword)](#PdfEncryptionDetails-java.lang.String-java.lang.String) | يقوم بتهيئة نسخة من هذه الفئة. |
| [PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions)](#PdfEncryptionDetails-java.lang.String-java.lang.String-int) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getOwnerPassword()](#getOwnerPassword) | يحدد كلمة مرور المالك للمستند PDF المشفر. |
| [getPermissions()](#getPermissions) | يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر. |
| [getUserPassword()](#getUserPassword) | يحدد كلمة مرور المستخدم المطلوبة لفتح المستند PDF المشفر. |
| [setOwnerPassword(String value)](#setOwnerPassword-java.lang.String) | يحدد كلمة مرور المالك للمستند PDF المشفر. |
| [setPermissions(int value)](#setPermissions-int) | يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر. |
| [setUserPassword(String value)](#setUserPassword-java.lang.String) | يحدد كلمة مرور المستخدم المطلوبة لفتح المستند PDF المشفر. |
### PdfEncryptionDetails(String userPassword, String ownerPassword) {#PdfEncryptionDetails-java.lang.String-java.lang.String}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword)
```


يقوم بتهيئة نسخة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |

### PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions) {#PdfEncryptionDetails-java.lang.String-java.lang.String-int}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |
| permissions | int |  |

### getOwnerPassword() {#getOwnerPassword}
```
public String getOwnerPassword()
```


يحدد كلمة مرور المالك للمستند PDF المشفر.

 **Remarks:** 

تسمح كلمة مرور المالك للمستخدم بفتح مستند PDF مشفر دون أي قيود وصول محددة في [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int).

لا يمكن أن تكون كلمة مرور المالك هي نفسها كلمة مرور المستخدم.

 **Examples:** 

يوضح كيفية تعيين الصلاحيات على مستند PDF محفوظ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getPermissions() {#getPermissions}
```
public int getPermissions()
```


يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر. القيمة الافتراضية هي [PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions/\#DISALLOW-ALL).

 **Examples:** 

يوضح كيفية تعيين الصلاحيات على مستند PDF محفوظ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Returns:**
int - القيمة المقابلة من نوع int. القيمة المرجعة هي تركيبة بتية من ثوابت [PdfPermissions](../../com.aspose.words/pdfpermissions/) .
### getUserPassword() {#getUserPassword}
```
public String getUserPassword()
```


يحدد كلمة مرور المستخدم المطلوبة لفتح المستند PDF المشفر.

 **Remarks:** 

ستكون كلمة مرور المستخدم مطلوبة لفتح مستند PDF مشفر للعرض. سيتم تطبيق الصلاحيات المحددة في [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) بواسطة برنامج القارئ.

يمكن أن تكون كلمة مرور المستخدم  null  أو سلسلة فارغة، وفي هذه الحالة لن يُطلب أي كلمة مرور من المستخدم عند فتح مستند PDF. لا يمكن أن تكون كلمة مرور المستخدم هي نفسها كلمة مرور المالك.

 **Examples:** 

يوضح كيفية تعيين الصلاحيات على مستند PDF محفوظ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### setOwnerPassword(String value) {#setOwnerPassword-java.lang.String}
```
public void setOwnerPassword(String value)
```


يحدد كلمة مرور المالك للمستند PDF المشفر.

 **Remarks:** 

تسمح كلمة مرور المالك للمستخدم بفتح مستند PDF مشفر دون أي قيود وصول محددة في [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int).

لا يمكن أن تكون كلمة مرور المالك هي نفسها كلمة مرور المستخدم.

 **Examples:** 

يوضح كيفية تعيين الصلاحيات على مستند PDF محفوظ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setPermissions(int value) {#setPermissions-int}
```
public void setPermissions(int value)
```


يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر. القيمة الافتراضية هي [PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions/\#DISALLOW-ALL).

 **Examples:** 

يوضح كيفية تعيين الصلاحيات على مستند PDF محفوظ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة المقابلة من نوع int. يجب أن تكون القيمة تركيبة بتية من ثوابت [PdfPermissions](../../com.aspose.words/pdfpermissions/). |

### setUserPassword(String value) {#setUserPassword-java.lang.String}
```
public void setUserPassword(String value)
```


يحدد كلمة مرور المستخدم المطلوبة لفتح المستند PDF المشفر.

 **Remarks:** 

ستكون كلمة مرور المستخدم مطلوبة لفتح مستند PDF مشفر للعرض. سيتم تطبيق الصلاحيات المحددة في [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\#setPermissions-int) بواسطة برنامج القارئ.

يمكن أن تكون كلمة مرور المستخدم  null  أو سلسلة فارغة، وفي هذه الحالة لن يُطلب أي كلمة مرور من المستخدم عند فتح مستند PDF. لا يمكن أن تكون كلمة مرور المستخدم هي نفسها كلمة مرور المالك.

 **Examples:** 

يوضح كيفية تعيين الصلاحيات على مستند PDF محفوظ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");

 // Extend permissions to allow the editing of annotations.
 PdfEncryptionDetails encryptionDetails =
         new PdfEncryptionDetails("password", "", PdfPermissions.MODIFY_ANNOTATIONS | PdfPermissions.DOCUMENT_ASSEMBLY);

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Enable encryption via the "EncryptionDetails" property.
 saveOptions.setEncryptionDetails(encryptionDetails);

 // When we open this document, we will need to provide the password before accessing its contents.
 doc.save(getArtifactsDir() + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

