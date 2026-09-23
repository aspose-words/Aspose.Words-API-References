---
title: "PdfEncryptionDetails"
linktitle: "PdfEncryptionDetails"
second_title: "Aspose.Words для Java"
description: "Содержит детали шифрования и разрешений доступа для PDF‑документа в Java."
type: docs
weight: 534
url: /ru/java/com.aspose.words/pdfencryptiondetails/
---

**Inheritance:**
java.lang.Object
```
public class PdfEncryptionDetails
```

Содержит детали шифрования и прав доступа к PDF‑документу.

Чтобы узнать больше, посетите статью документации [ Protect or Encrypt a Document ][Protect or Encrypt a Document].

 **Examples:** 

Показывает, как установить разрешения для сохранённого PDF‑документа.

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
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [PdfEncryptionDetails(String userPassword, String ownerPassword)](#PdfEncryptionDetails-java.lang.String-java.lang.String) | Инициализирует экземпляр этого класса. |
| [PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions)](#PdfEncryptionDetails-java.lang.String-java.lang.String-int) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [getOwnerPassword()](#getOwnerPassword) | Указывает пароль владельца для зашифрованного PDF‑документа. |
| [getPermissions()](#getPermissions) | Указывает операции, разрешённые пользователю в зашифрованном PDF‑документе. |
| [getUserPassword()](#getUserPassword) | Указывает пароль пользователя, необходимый для открытия зашифрованного PDF‑документа. |
| [setOwnerPassword(String value)](#setOwnerPassword-java.lang.String) | Указывает пароль владельца для зашифрованного PDF‑документа. |
| [setPermissions(int value)](#setPermissions-int) | Указывает операции, разрешённые пользователю в зашифрованном PDF‑документе. |
| [setUserPassword(String value)](#setUserPassword-java.lang.String) | Указывает пароль пользователя, необходимый для открытия зашифрованного PDF‑документа. |
### PdfEncryptionDetails(String userPassword, String ownerPassword) {#PdfEncryptionDetails-java.lang.String-java.lang.String}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword)
```


Инициализирует экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |

### PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions) {#PdfEncryptionDetails-java.lang.String-java.lang.String-int}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword, int permissions)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |
| permissions | int |  |

### getOwnerPassword() {#getOwnerPassword}
```
public String getOwnerPassword()
```


Указывает пароль владельца для зашифрованного PDF‑документа.

 **Remarks:** 

Пароль владельца позволяет пользователю открыть зашифрованный PDF‑документ без каких-либо ограничений доступа, указанных в [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\\#setPermissions-int).

Пароль владельца не может совпадать с паролем пользователя.

 **Examples:** 

Показывает, как установить разрешения для сохранённого PDF‑документа.

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
java.lang.String - Соответствующее значение java.lang.String.
### getPermissions() {#getPermissions}
```
public int getPermissions()
```


Указывает операции, разрешённые пользователю на зашифрованном PDF‑документе. Значение по умолчанию — [PdfPermissions.DISALLOW\\_ALL](../../com.aspose.words/pdfpermissions/\\#DISALLOW-ALL).

 **Examples:** 

Показывает, как установить разрешения для сохранённого PDF‑документа.

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
int - Соответствующее значение  int . Возвращаемое значение является побитовой комбинацией констант [PdfPermissions](../../com.aspose.words/pdfpermissions/).
### getUserPassword() {#getUserPassword}
```
public String getUserPassword()
```


Указывает пароль пользователя, необходимый для открытия зашифрованного PDF‑документа.

 **Remarks:** 

Пароль пользователя будет требоваться для открытия зашифрованного PDF‑документа для просмотра. Разрешения, указанные в [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\\#setPermissions-int), будут применяться программным обеспечением чтения.

Пароль пользователя может быть  null  или пустой строкой; в этом случае пароль от пользователя не требуется при открытии PDF‑документа. Пароль пользователя не может совпадать с паролем владельца.

 **Examples:** 

Показывает, как установить разрешения для сохранённого PDF‑документа.

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
java.lang.String - Соответствующее значение java.lang.String.
### setOwnerPassword(String value) {#setOwnerPassword-java.lang.String}
```
public void setOwnerPassword(String value)
```


Указывает пароль владельца для зашифрованного PDF‑документа.

 **Remarks:** 

Пароль владельца позволяет пользователю открыть зашифрованный PDF‑документ без каких-либо ограничений доступа, указанных в [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\\#setPermissions-int).

Пароль владельца не может совпадать с паролем пользователя.

 **Examples:** 

Показывает, как установить разрешения для сохранённого PDF‑документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setPermissions(int value) {#setPermissions-int}
```
public void setPermissions(int value)
```


Указывает операции, разрешённые пользователю на зашифрованном PDF‑документе. Значение по умолчанию — [PdfPermissions.DISALLOW\\_ALL](../../com.aspose.words/pdfpermissions/\\#DISALLOW-ALL).

 **Examples:** 

Показывает, как установить разрешения для сохранённого PDF‑документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее значение  int . Значение должно быть побитовой комбинацией констант [PdfPermissions](../../com.aspose.words/pdfpermissions/). |

### setUserPassword(String value) {#setUserPassword-java.lang.String}
```
public void setUserPassword(String value)
```


Указывает пароль пользователя, необходимый для открытия зашифрованного PDF‑документа.

 **Remarks:** 

Пароль пользователя будет требоваться для открытия зашифрованного PDF‑документа для просмотра. Разрешения, указанные в [getPermissions()](../../com.aspose.words/pdfencryptiondetails/\\#getPermissions) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails/\\#setPermissions-int), будут применяться программным обеспечением чтения.

Пароль пользователя может быть  null  или пустой строкой; в этом случае пароль от пользователя не требуется при открытии PDF‑документа. Пароль пользователя не может совпадать с паролем владельца.

 **Examples:** 

Показывает, как установить разрешения для сохранённого PDF‑документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

