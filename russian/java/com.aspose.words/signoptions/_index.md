---
title: "SignOptions"
linktitle: "SignOptions"
second_title: "Aspose.Words для Java"
description: "Позволяет задавать параметры подписи документа в Java."
type: docs
weight: 620
url: /ru/java/com.aspose.words/signoptions/
---

**Inheritance:**
java.lang.Object
```
public class SignOptions
```

Позволяет указать параметры подписи документа.

Чтобы узнать больше, посетите статью документации [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

Показывает, как цифрово подписывать документы.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment and date which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("My comment");
     signOptions.setSignTime(new Date());
 }

 // Take an unsigned document from the local file system via a file stream,
 // then create a signed copy of it determined by the filename of the output file stream.
 InputStream streamIn = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream streamOut = new FileOutputStream(getArtifactsDir() + "DigitalSignatureUtil.SignDocument.docx");
     try {
         DigitalSignatureUtil.sign(streamIn, streamOut, certificateHolder, signOptions);
     } finally {
         if (streamOut != null) streamOut.close();
     }
 } finally {
     if (streamIn != null) streamIn.close();
 }
 
```


[Work with Digital Signatures]: https://docs.aspose.com/words/java/working-with-digital-signatures/
## Методы

| Метод | Описание |
| --- | --- |
| [getApplicationVersion()](#getApplicationVersion) | Получает версию приложения для цифровой подписи. |
| [getColorDepth()](#getColorDepth) | Получает глубину цвета для цифровой подписи. |
| [getComments()](#getComments) | Указывает комментарии к цифровой подписи. |
| [getDecryptionPassword()](#getDecryptionPassword) | Пароль для расшифровки исходного документа. |
| [getHorizontalResolution()](#getHorizontalResolution) | Получает горизонтальное разрешение цифровой подписи. |
| [getOfficeVersion()](#getOfficeVersion) | Получает версию Office для цифровой подписи. |
| [getProviderId()](#getProviderId) | Указывает идентификатор класса поставщика подписи. |
| [getSignTime()](#getSignTime) | Дата подписи. |
| [getSignatureLineId()](#getSignatureLineId) | Идентификатор строки подписи. |
| [getSignatureLineImage()](#getSignatureLineImage) | Изображение, которое будет отображаться в связанной [SignatureLine](../../com.aspose.words/signatureline/). |
| [getVerticalResolution()](#getVerticalResolution) | Получает вертикальное разрешение цифровой подписи. |
| [getWindowsVersion()](#getWindowsVersion) | Получает версию Windows для цифровой подписи. |
| [getXmlDsigLevel()](#getXmlDsigLevel) | Указывает уровень цифровой подписи в соответствии со стандартом XML-DSig. |
| [setApplicationVersion(String value)](#setApplicationVersion-java.lang.String) | Устанавливает версию приложения для цифровой подписи. |
| [setColorDepth(int value)](#setColorDepth-int) | Устанавливает глубину цвета для цифровой подписи. |
| [setComments(String value)](#setComments-java.lang.String) | Указывает комментарии к цифровой подписи. |
| [setDecryptionPassword(String value)](#setDecryptionPassword-java.lang.String) | Пароль для расшифровки исходного документа. |
| [setHorizontalResolution(int value)](#setHorizontalResolution-int) | Устанавливает горизонтальное разрешение для цифровой подписи. |
| [setOfficeVersion(String value)](#setOfficeVersion-java.lang.String) | Устанавливает версию Office для цифровой подписи. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID) | Указывает идентификатор класса поставщика подписи. |
| [setSignTime(Date value)](#setSignTime-java.util.Date) | Дата подписи. |
| [setSignatureLineId(UUID value)](#setSignatureLineId-java.util.UUID) | Идентификатор строки подписи. |
| [setSignatureLineImage(byte[] value)](#setSignatureLineImage-byte) | Изображение, которое будет отображаться в связанной [SignatureLine](../../com.aspose.words/signatureline/). |
| [setVerticalResolution(int value)](#setVerticalResolution-int) | Устанавливает вертикальное разрешение для цифровой подписи. |
| [setWindowsVersion(String value)](#setWindowsVersion-java.lang.String) | Устанавливает версию Windows для цифровой подписи. |
| [setXmlDsigLevel(int value)](#setXmlDsigLevel-int) | Указывает уровень цифровой подписи в соответствии со стандартом XML-DSig. |
### getApplicationVersion() {#getApplicationVersion}
```
public String getApplicationVersion()
```


Получает версию приложения для цифровой подписи. Значение по умолчанию — "12.0".

 **Examples:** 

Показывает, как подписать документ с дополнительными параметрами подписи.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setWindowsVersion("10.0");
     signOptions.setApplicationVersion("16.0.19127");
     signOptions.setOfficeVersion("16.0.19127/27");
     signOptions.setHorizontalResolution(1024);
     signOptions.setVerticalResolution(768);
     signOptions.setColorDepth(24);
 }

 byte[] certBytes = Files.readAllBytes(Paths.get(getMyDir() + "morzal.pfx"));
 CertificateHolder cert = CertificateHolder.create(certBytes, "aw");
 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.docx");

 DigitalSignature signature = signedDoc.getDigitalSignatures().get(0);
 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signature.isValid());
 Assert.assertEquals("10.0", signature.getWindowsVersion());
 Assert.assertEquals("16.0.19127", signature.getApplicationVersion());
 Assert.assertEquals("16.0.19127/27", signature.getOfficeVersion());
 Assert.assertEquals(1024, signature.getHorizontalResolution());
 Assert.assertEquals(768, signature.getVerticalResolution());
 Assert.assertEquals(24, signature.getColorDepth());
 
```

**Returns:**
java.lang.String — версия приложения для цифровой подписи.
### getColorDepth() {#getColorDepth}
```
public int getColorDepth()
```


Получает глубину цвета для цифровой подписи. Значение по умолчанию — 32.

 **Examples:** 

Показывает, как подписать документ с дополнительными параметрами подписи.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setWindowsVersion("10.0");
     signOptions.setApplicationVersion("16.0.19127");
     signOptions.setOfficeVersion("16.0.19127/27");
     signOptions.setHorizontalResolution(1024);
     signOptions.setVerticalResolution(768);
     signOptions.setColorDepth(24);
 }

 byte[] certBytes = Files.readAllBytes(Paths.get(getMyDir() + "morzal.pfx"));
 CertificateHolder cert = CertificateHolder.create(certBytes, "aw");
 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.docx");

 DigitalSignature signature = signedDoc.getDigitalSignatures().get(0);
 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signature.isValid());
 Assert.assertEquals("10.0", signature.getWindowsVersion());
 Assert.assertEquals("16.0.19127", signature.getApplicationVersion());
 Assert.assertEquals("16.0.19127/27", signature.getOfficeVersion());
 Assert.assertEquals(1024, signature.getHorizontalResolution());
 Assert.assertEquals(768, signature.getVerticalResolution());
 Assert.assertEquals(24, signature.getColorDepth());
 
```

**Returns:**
int — глубина цвета для цифровой подписи.
### getComments() {#getComments}
```
public String getComments()
```


Указывает комментарии к цифровой подписи. Значение по умолчанию — **empty string**.

 **Examples:** 

Показывает, как цифрово подписывать документы.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment and date which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("My comment");
     signOptions.setSignTime(new Date());
 }

 // Take an unsigned document from the local file system via a file stream,
 // then create a signed copy of it determined by the filename of the output file stream.
 InputStream streamIn = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream streamOut = new FileOutputStream(getArtifactsDir() + "DigitalSignatureUtil.SignDocument.docx");
     try {
         DigitalSignatureUtil.sign(streamIn, streamOut, certificateHolder, signOptions);
     } finally {
         if (streamOut != null) streamOut.close();
     }
 } finally {
     if (streamIn != null) streamIn.close();
 }
 
```

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getDecryptionPassword() {#getDecryptionPassword}
```
public String getDecryptionPassword()
```


Пароль для расшифровки исходного документа. Значение по умолчанию — **empty string**.

 **Remarks:** 

Если документ OOXML зашифрован, необходимо предоставить пароль для расшифровки исходного документа перед его подписанием. Это не требуется для документов в бинарном формате DOC.

 **Examples:** 

Показывает, как подписать зашифрованный файл документа.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment, date, and decryption password which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("Comment");
     signOptions.setSignTime(new Date());
     signOptions.setDecryptionPassword("docPassword");
 }

 // Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
 String inputFileName = getMyDir() + "Encrypted.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.DecryptionPassword.docx";

 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getHorizontalResolution() {#getHorizontalResolution}
```
public int getHorizontalResolution()
```


Получает горизонтальное разрешение цифровой подписи. Значение по умолчанию — 1920.

 **Examples:** 

Показывает, как подписать документ с дополнительными параметрами подписи.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setWindowsVersion("10.0");
     signOptions.setApplicationVersion("16.0.19127");
     signOptions.setOfficeVersion("16.0.19127/27");
     signOptions.setHorizontalResolution(1024);
     signOptions.setVerticalResolution(768);
     signOptions.setColorDepth(24);
 }

 byte[] certBytes = Files.readAllBytes(Paths.get(getMyDir() + "morzal.pfx"));
 CertificateHolder cert = CertificateHolder.create(certBytes, "aw");
 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.docx");

 DigitalSignature signature = signedDoc.getDigitalSignatures().get(0);
 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signature.isValid());
 Assert.assertEquals("10.0", signature.getWindowsVersion());
 Assert.assertEquals("16.0.19127", signature.getApplicationVersion());
 Assert.assertEquals("16.0.19127/27", signature.getOfficeVersion());
 Assert.assertEquals(1024, signature.getHorizontalResolution());
 Assert.assertEquals(768, signature.getVerticalResolution());
 Assert.assertEquals(24, signature.getColorDepth());
 
```

**Returns:**
int — горизонтальное разрешение цифровой подписи.
### getOfficeVersion() {#getOfficeVersion}
```
public String getOfficeVersion()
```


Получает версию Office для цифровой подписи. Значение по умолчанию — "12.0".

 **Examples:** 

Показывает, как подписать документ с дополнительными параметрами подписи.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setWindowsVersion("10.0");
     signOptions.setApplicationVersion("16.0.19127");
     signOptions.setOfficeVersion("16.0.19127/27");
     signOptions.setHorizontalResolution(1024);
     signOptions.setVerticalResolution(768);
     signOptions.setColorDepth(24);
 }

 byte[] certBytes = Files.readAllBytes(Paths.get(getMyDir() + "morzal.pfx"));
 CertificateHolder cert = CertificateHolder.create(certBytes, "aw");
 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.docx");

 DigitalSignature signature = signedDoc.getDigitalSignatures().get(0);
 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signature.isValid());
 Assert.assertEquals("10.0", signature.getWindowsVersion());
 Assert.assertEquals("16.0.19127", signature.getApplicationVersion());
 Assert.assertEquals("16.0.19127/27", signature.getOfficeVersion());
 Assert.assertEquals(1024, signature.getHorizontalResolution());
 Assert.assertEquals(768, signature.getVerticalResolution());
 Assert.assertEquals(24, signature.getColorDepth());
 
```

**Returns:**
java.lang.String — версия Office для цифровой подписи.
### getProviderId() {#getProviderId}
```
public UUID getProviderId()
```


Указывает идентификатор класса поставщика подписи. Значение по умолчанию — **Empty (all zeroes) Guid**.

 **Remarks:** 

Криптографический сервисный провайдер (CSP) — независимый программный модуль, который фактически выполняет криптографические алгоритмы для аутентификации, кодирования и шифрования. MS Office резервирует значение \{00000000-0000-0000-0000-000000000000\} для своего провайдера подписи по умолчанию.

GUID дополнительно установленного провайдера следует получить из документации, поставляемой с провайдером.

Кроме того, все установленные криптографические провайдеры перечислены в реестре Windows. Их можно найти по следующему пути: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. Существует имя ключа "CP Service UUID", которое соответствует GUID провайдера подписи.

 **Examples:** 

Показывает, как подписать документ с помощью личного сертификата и строки подписи.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
 signatureLineOptions.setSigner("vderyushev");
 signatureLineOptions.setSignerTitle("QA");
 signatureLineOptions.setEmail("vderyushev@aspose.com");
 signatureLineOptions.setShowDate(true);
 signatureLineOptions.setDefaultInstructions(false);
 signatureLineOptions.setInstructions("Please sign here.");
 signatureLineOptions.setAllowComments(true);

 SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
 signatureLine.setProviderId(UUID.fromString("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

 Assert.assertFalse(signatureLine.isSigned());
 Assert.assertFalse(signatureLine.isValid());

 doc.save(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx");

 Date currentDate = new Date();

 SignOptions signOptions = new SignOptions();
 signOptions.setSignatureLineId(signatureLine.getId());
 signOptions.setProviderId(signatureLine.getProviderId());
 signOptions.setComments("Document was signed by vderyushev");
 signOptions.setSignTime(currentDate);

 CertificateHolder certHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx",
         getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

 // Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
 // indicating that the signature line contains a signature.
 doc = new Document(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 signatureLine = shape.getSignatureLine();

 Assert.assertTrue(signatureLine.isSigned());
 Assert.assertTrue(signatureLine.isValid());
 
```

**Returns:**
java.util.UUID — соответствующее значение java.util.UUID.
### getSignTime() {#getSignTime}
```
public Date getSignTime()
```


Дата подписи. Значение по умолчанию — **current time**.

 **Examples:** 

Показывает, как цифрово подписывать документы.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment and date which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("My comment");
     signOptions.setSignTime(new Date());
 }

 // Take an unsigned document from the local file system via a file stream,
 // then create a signed copy of it determined by the filename of the output file stream.
 InputStream streamIn = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream streamOut = new FileOutputStream(getArtifactsDir() + "DigitalSignatureUtil.SignDocument.docx");
     try {
         DigitalSignatureUtil.sign(streamIn, streamOut, certificateHolder, signOptions);
     } finally {
         if (streamOut != null) streamOut.close();
     }
 } finally {
     if (streamIn != null) streamIn.close();
 }
 
```

**Returns:**
java.util.Date — соответствующее значение java.util.Date.
### getSignatureLineId() {#getSignatureLineId}
```
public UUID getSignatureLineId()
```


Идентификатор строки подписи. Значение по умолчанию — **Empty (all zeroes) Guid**.

 **Remarks:** 

При установке он связывает [SignatureLine](../../com.aspose.words/signatureline/) с соответствующей [DigitalSignature](../../com.aspose.words/digitalsignature/).

 **Examples:** 

Показывает, как добавить строку подписи в документ, а затем подписать его с помощью цифрового сертификата.

```

 public static void sign() throws Exception {
     String signPersonName = "Ron Williams";
     String srcDocumentPath = getMyDir() + "Document.docx";
     String dstDocumentPath = getArtifactsDir() + "SignDocumentCustom.Sign.docx";
     String certificatePath = getMyDir() + "morzal.pfx";
     String certificatePassword = "aw";

     // We need to create simple list with test signers for this example.
     createSignPersonData();
     System.out.println("Test data successfully added!");

     // Get sign person object by name of the person who must sign a document.
     // This an example, in real use case you would return an object from a database.
     SignPersonTestClass signPersonInfo = gSignPersonList.stream().filter(x -> x.getName() == signPersonName).findFirst().get();

     if (signPersonInfo != null) {
         signDocument(srcDocumentPath, dstDocumentPath, signPersonInfo, certificatePath, certificatePassword);
         System.out.println("Document successfully signed!");
     } else {
         System.out.println("Sign person does not exist, please check your parameters.");
     }

     // Now do something with a signed document, for example, save it to your database.
     // Use 'new Document(dstDocumentPath)' for loading a signed document.
 }

 /// 
 /// Signs the document obtained at the source location and saves it to the specified destination.
 /// 
 private static void signDocument(final String srcDocumentPath, final String dstDocumentPath,
                                  final SignPersonTestClass signPersonInfo, final String certificatePath,
                                  final String certificatePassword) throws Exception {
     // Create new document instance based on a test file that we need to sign.
     Document document = new Document(srcDocumentPath);
     DocumentBuilder builder = new DocumentBuilder(document);

     // Add info about responsible person who sign a document.
     SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
     signatureLineOptions.setSigner(signPersonInfo.getName());
     signatureLineOptions.setSignerTitle(signPersonInfo.getPosition());

     // Add signature line for responsible person who sign a document.
     SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
     signatureLine.setId(signPersonInfo.getPersonId());

     // Save a document with line signatures into temporary file for future signing.
     builder.getDocument().save(dstDocumentPath);

     // Create holder of certificate instance based on your personal certificate.
     // This is the test certificate generated for this example.
     CertificateHolder certificateHolder = CertificateHolder.create(certificatePath, certificatePassword);

     // Link our signature line with personal signature.
     SignOptions signOptions = new SignOptions();
     signOptions.setSignatureLineId(signPersonInfo.getPersonId());
     signOptions.setSignatureLineImage(signPersonInfo.getImage());

     // Sign a document which contains signature line with personal certificate.
     DigitalSignatureUtil.sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
 }

 /// 
 /// Create test data that contains info about sing persons.
 /// 
 private static void createSignPersonData() throws IOException {
     InputStream inputStream = new FileInputStream(getImageDir() + "Logo.jpg");

     gSignPersonList = new ArrayList<>();
     gSignPersonList.add(new SignPersonTestClass(UUID.randomUUID(), "Ron Williams", "Chief Executive Officer",
             DocumentHelper.getBytesFromStream(inputStream)));
     gSignPersonList.add(new SignPersonTestClass(UUID.randomUUID(), "Stephen Morse", "Head of Compliance",
             DocumentHelper.getBytesFromStream(inputStream)));
 }

 private static ArrayList gSignPersonList;
 
```

**Returns:**
java.util.UUID — соответствующее значение java.util.UUID.
### getSignatureLineImage() {#getSignatureLineImage}
```
public byte[] getSignatureLineImage()
```


Изображение, которое будет отображаться в связанной [SignatureLine](../../com.aspose.words/signatureline/). Значение по умолчанию — null.

 **Examples:** 

Показывает, как добавить строку подписи в документ, а затем подписать его с помощью цифрового сертификата.

```

 public static void sign() throws Exception {
     String signPersonName = "Ron Williams";
     String srcDocumentPath = getMyDir() + "Document.docx";
     String dstDocumentPath = getArtifactsDir() + "SignDocumentCustom.Sign.docx";
     String certificatePath = getMyDir() + "morzal.pfx";
     String certificatePassword = "aw";

     // We need to create simple list with test signers for this example.
     createSignPersonData();
     System.out.println("Test data successfully added!");

     // Get sign person object by name of the person who must sign a document.
     // This an example, in real use case you would return an object from a database.
     SignPersonTestClass signPersonInfo = gSignPersonList.stream().filter(x -> x.getName() == signPersonName).findFirst().get();

     if (signPersonInfo != null) {
         signDocument(srcDocumentPath, dstDocumentPath, signPersonInfo, certificatePath, certificatePassword);
         System.out.println("Document successfully signed!");
     } else {
         System.out.println("Sign person does not exist, please check your parameters.");
     }

     // Now do something with a signed document, for example, save it to your database.
     // Use 'new Document(dstDocumentPath)' for loading a signed document.
 }

 /// 
 /// Signs the document obtained at the source location and saves it to the specified destination.
 /// 
 private static void signDocument(final String srcDocumentPath, final String dstDocumentPath,
                                  final SignPersonTestClass signPersonInfo, final String certificatePath,
                                  final String certificatePassword) throws Exception {
     // Create new document instance based on a test file that we need to sign.
     Document document = new Document(srcDocumentPath);
     DocumentBuilder builder = new DocumentBuilder(document);

     // Add info about responsible person who sign a document.
     SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
     signatureLineOptions.setSigner(signPersonInfo.getName());
     signatureLineOptions.setSignerTitle(signPersonInfo.getPosition());

     // Add signature line for responsible person who sign a document.
     SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
     signatureLine.setId(signPersonInfo.getPersonId());

     // Save a document with line signatures into temporary file for future signing.
     builder.getDocument().save(dstDocumentPath);

     // Create holder of certificate instance based on your personal certificate.
     // This is the test certificate generated for this example.
     CertificateHolder certificateHolder = CertificateHolder.create(certificatePath, certificatePassword);

     // Link our signature line with personal signature.
     SignOptions signOptions = new SignOptions();
     signOptions.setSignatureLineId(signPersonInfo.getPersonId());
     signOptions.setSignatureLineImage(signPersonInfo.getImage());

     // Sign a document which contains signature line with personal certificate.
     DigitalSignatureUtil.sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
 }

 /// 
 /// Create test data that contains info about sing persons.
 /// 
 private static void createSignPersonData() throws IOException {
     InputStream inputStream = new FileInputStream(getImageDir() + "Logo.jpg");

     gSignPersonList = new ArrayList<>();
     gSignPersonList.add(new SignPersonTestClass(UUID.randomUUID(), "Ron Williams", "Chief Executive Officer",
             DocumentHelper.getBytesFromStream(inputStream)));
     gSignPersonList.add(new SignPersonTestClass(UUID.randomUUID(), "Stephen Morse", "Head of Compliance",
             DocumentHelper.getBytesFromStream(inputStream)));
 }

 private static ArrayList gSignPersonList;
 
```

**Returns:**
byte[] — соответствующее значение byte[].
### getVerticalResolution() {#getVerticalResolution}
```
public int getVerticalResolution()
```


Получает вертикальное разрешение для цифровой подписи. Значение по умолчанию — 1200.

 **Examples:** 

Показывает, как подписать документ с дополнительными параметрами подписи.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setWindowsVersion("10.0");
     signOptions.setApplicationVersion("16.0.19127");
     signOptions.setOfficeVersion("16.0.19127/27");
     signOptions.setHorizontalResolution(1024);
     signOptions.setVerticalResolution(768);
     signOptions.setColorDepth(24);
 }

 byte[] certBytes = Files.readAllBytes(Paths.get(getMyDir() + "morzal.pfx"));
 CertificateHolder cert = CertificateHolder.create(certBytes, "aw");
 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.docx");

 DigitalSignature signature = signedDoc.getDigitalSignatures().get(0);
 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signature.isValid());
 Assert.assertEquals("10.0", signature.getWindowsVersion());
 Assert.assertEquals("16.0.19127", signature.getApplicationVersion());
 Assert.assertEquals("16.0.19127/27", signature.getOfficeVersion());
 Assert.assertEquals(1024, signature.getHorizontalResolution());
 Assert.assertEquals(768, signature.getVerticalResolution());
 Assert.assertEquals(24, signature.getColorDepth());
 
```

**Returns:**
int — вертикальное разрешение для цифровой подписи.
### getWindowsVersion() {#getWindowsVersion}
```
public String getWindowsVersion()
```


Получает версию Windows для цифровой подписи. Значение по умолчанию — "6.1".

 **Examples:** 

Показывает, как подписать документ с дополнительными параметрами подписи.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setWindowsVersion("10.0");
     signOptions.setApplicationVersion("16.0.19127");
     signOptions.setOfficeVersion("16.0.19127/27");
     signOptions.setHorizontalResolution(1024);
     signOptions.setVerticalResolution(768);
     signOptions.setColorDepth(24);
 }

 byte[] certBytes = Files.readAllBytes(Paths.get(getMyDir() + "morzal.pfx"));
 CertificateHolder cert = CertificateHolder.create(certBytes, "aw");
 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.docx");

 DigitalSignature signature = signedDoc.getDigitalSignatures().get(0);
 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signature.isValid());
 Assert.assertEquals("10.0", signature.getWindowsVersion());
 Assert.assertEquals("16.0.19127", signature.getApplicationVersion());
 Assert.assertEquals("16.0.19127/27", signature.getOfficeVersion());
 Assert.assertEquals(1024, signature.getHorizontalResolution());
 Assert.assertEquals(768, signature.getVerticalResolution());
 Assert.assertEquals(24, signature.getColorDepth());
 
```

**Returns:**
java.lang.String — версия Windows для цифровой подписи.
### getXmlDsigLevel() {#getXmlDsigLevel}
```
public int getXmlDsigLevel()
```


Указывает уровень цифровой подписи на основе стандарта XML-DSig. Значение по умолчанию — [XmlDsigLevel.XML\_D\_SIG](../../com.aspose.words/xmldsiglevel/\#XML-D-SIG).

 **Remarks:** 

Различные уровни подписей XAdES могут быть созданы, начиная с Office 2010.

 **Examples:** 

Показывает, как подписать документ на основе стандарта XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Returns:**
int — соответствующее  int  значение. Возвращаемое значение является одной из констант [XmlDsigLevel](../../com.aspose.words/xmldsiglevel/).
### setApplicationVersion(String value) {#setApplicationVersion-java.lang.String}
```
public void setApplicationVersion(String value)
```


Устанавливает версию приложения для цифровой подписи. Значение по умолчанию — "12.0".

 **Examples:** 

Показывает, как подписать документ с дополнительными параметрами подписи.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setWindowsVersion("10.0");
     signOptions.setApplicationVersion("16.0.19127");
     signOptions.setOfficeVersion("16.0.19127/27");
     signOptions.setHorizontalResolution(1024);
     signOptions.setVerticalResolution(768);
     signOptions.setColorDepth(24);
 }

 byte[] certBytes = Files.readAllBytes(Paths.get(getMyDir() + "morzal.pfx"));
 CertificateHolder cert = CertificateHolder.create(certBytes, "aw");
 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.docx");

 DigitalSignature signature = signedDoc.getDigitalSignatures().get(0);
 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signature.isValid());
 Assert.assertEquals("10.0", signature.getWindowsVersion());
 Assert.assertEquals("16.0.19127", signature.getApplicationVersion());
 Assert.assertEquals("16.0.19127/27", signature.getOfficeVersion());
 Assert.assertEquals(1024, signature.getHorizontalResolution());
 Assert.assertEquals(768, signature.getVerticalResolution());
 Assert.assertEquals(24, signature.getColorDepth());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Версия приложения для цифровой подписи. |

### setColorDepth(int value) {#setColorDepth-int}
```
public void setColorDepth(int value)
```


Устанавливает глубину цвета для цифровой подписи. Значение по умолчанию — 32.

 **Examples:** 

Показывает, как подписать документ с дополнительными параметрами подписи.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setWindowsVersion("10.0");
     signOptions.setApplicationVersion("16.0.19127");
     signOptions.setOfficeVersion("16.0.19127/27");
     signOptions.setHorizontalResolution(1024);
     signOptions.setVerticalResolution(768);
     signOptions.setColorDepth(24);
 }

 byte[] certBytes = Files.readAllBytes(Paths.get(getMyDir() + "morzal.pfx"));
 CertificateHolder cert = CertificateHolder.create(certBytes, "aw");
 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.docx");

 DigitalSignature signature = signedDoc.getDigitalSignatures().get(0);
 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signature.isValid());
 Assert.assertEquals("10.0", signature.getWindowsVersion());
 Assert.assertEquals("16.0.19127", signature.getApplicationVersion());
 Assert.assertEquals("16.0.19127/27", signature.getOfficeVersion());
 Assert.assertEquals(1024, signature.getHorizontalResolution());
 Assert.assertEquals(768, signature.getVerticalResolution());
 Assert.assertEquals(24, signature.getColorDepth());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Глубина цвета для цифровой подписи. |

### setComments(String value) {#setComments-java.lang.String}
```
public void setComments(String value)
```


Указывает комментарии к цифровой подписи. Значение по умолчанию — **empty string**.

 **Examples:** 

Показывает, как цифрово подписывать документы.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment and date which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("My comment");
     signOptions.setSignTime(new Date());
 }

 // Take an unsigned document from the local file system via a file stream,
 // then create a signed copy of it determined by the filename of the output file stream.
 InputStream streamIn = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream streamOut = new FileOutputStream(getArtifactsDir() + "DigitalSignatureUtil.SignDocument.docx");
     try {
         DigitalSignatureUtil.sign(streamIn, streamOut, certificateHolder, signOptions);
     } finally {
         if (streamOut != null) streamOut.close();
     }
 } finally {
     if (streamIn != null) streamIn.close();
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setDecryptionPassword(String value) {#setDecryptionPassword-java.lang.String}
```
public void setDecryptionPassword(String value)
```


Пароль для расшифровки исходного документа. Значение по умолчанию — **empty string**.

 **Remarks:** 

Если документ OOXML зашифрован, необходимо предоставить пароль для расшифровки исходного документа перед его подписанием. Это не требуется для документов в бинарном формате DOC.

 **Examples:** 

Показывает, как подписать зашифрованный файл документа.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment, date, and decryption password which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("Comment");
     signOptions.setSignTime(new Date());
     signOptions.setDecryptionPassword("docPassword");
 }

 // Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
 String inputFileName = getMyDir() + "Encrypted.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.DecryptionPassword.docx";

 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setHorizontalResolution(int value) {#setHorizontalResolution-int}
```
public void setHorizontalResolution(int value)
```


Устанавливает горизонтальное разрешение для цифровой подписи. Значение по умолчанию — 1920.

 **Examples:** 

Показывает, как подписать документ с дополнительными параметрами подписи.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setWindowsVersion("10.0");
     signOptions.setApplicationVersion("16.0.19127");
     signOptions.setOfficeVersion("16.0.19127/27");
     signOptions.setHorizontalResolution(1024);
     signOptions.setVerticalResolution(768);
     signOptions.setColorDepth(24);
 }

 byte[] certBytes = Files.readAllBytes(Paths.get(getMyDir() + "morzal.pfx"));
 CertificateHolder cert = CertificateHolder.create(certBytes, "aw");
 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.docx");

 DigitalSignature signature = signedDoc.getDigitalSignatures().get(0);
 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signature.isValid());
 Assert.assertEquals("10.0", signature.getWindowsVersion());
 Assert.assertEquals("16.0.19127", signature.getApplicationVersion());
 Assert.assertEquals("16.0.19127/27", signature.getOfficeVersion());
 Assert.assertEquals(1024, signature.getHorizontalResolution());
 Assert.assertEquals(768, signature.getVerticalResolution());
 Assert.assertEquals(24, signature.getColorDepth());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Горизонтальное разрешение для цифровой подписи. |

### setOfficeVersion(String value) {#setOfficeVersion-java.lang.String}
```
public void setOfficeVersion(String value)
```


Устанавливает версию Office для цифровой подписи. Значение по умолчанию — "12.0".

 **Examples:** 

Показывает, как подписать документ с дополнительными параметрами подписи.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setWindowsVersion("10.0");
     signOptions.setApplicationVersion("16.0.19127");
     signOptions.setOfficeVersion("16.0.19127/27");
     signOptions.setHorizontalResolution(1024);
     signOptions.setVerticalResolution(768);
     signOptions.setColorDepth(24);
 }

 byte[] certBytes = Files.readAllBytes(Paths.get(getMyDir() + "morzal.pfx"));
 CertificateHolder cert = CertificateHolder.create(certBytes, "aw");
 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.docx");

 DigitalSignature signature = signedDoc.getDigitalSignatures().get(0);
 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signature.isValid());
 Assert.assertEquals("10.0", signature.getWindowsVersion());
 Assert.assertEquals("16.0.19127", signature.getApplicationVersion());
 Assert.assertEquals("16.0.19127/27", signature.getOfficeVersion());
 Assert.assertEquals(1024, signature.getHorizontalResolution());
 Assert.assertEquals(768, signature.getVerticalResolution());
 Assert.assertEquals(24, signature.getColorDepth());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Версия Office для цифровой подписи. |

### setProviderId(UUID value) {#setProviderId-java.util.UUID}
```
public void setProviderId(UUID value)
```


Указывает идентификатор класса поставщика подписи. Значение по умолчанию — **Empty (all zeroes) Guid**.

 **Remarks:** 

Криптографический сервисный провайдер (CSP) — независимый программный модуль, который фактически выполняет криптографические алгоритмы для аутентификации, кодирования и шифрования. MS Office резервирует значение \{00000000-0000-0000-0000-000000000000\} для своего провайдера подписи по умолчанию.

GUID дополнительно установленного провайдера следует получить из документации, поставляемой с провайдером.

Кроме того, все установленные криптографические провайдеры перечислены в реестре Windows. Их можно найти по следующему пути: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. Существует имя ключа "CP Service UUID", которое соответствует GUID провайдера подписи.

 **Examples:** 

Показывает, как подписать документ с помощью личного сертификата и строки подписи.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
 signatureLineOptions.setSigner("vderyushev");
 signatureLineOptions.setSignerTitle("QA");
 signatureLineOptions.setEmail("vderyushev@aspose.com");
 signatureLineOptions.setShowDate(true);
 signatureLineOptions.setDefaultInstructions(false);
 signatureLineOptions.setInstructions("Please sign here.");
 signatureLineOptions.setAllowComments(true);

 SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
 signatureLine.setProviderId(UUID.fromString("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

 Assert.assertFalse(signatureLine.isSigned());
 Assert.assertFalse(signatureLine.isValid());

 doc.save(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx");

 Date currentDate = new Date();

 SignOptions signOptions = new SignOptions();
 signOptions.setSignatureLineId(signatureLine.getId());
 signOptions.setProviderId(signatureLine.getProviderId());
 signOptions.setComments("Document was signed by vderyushev");
 signOptions.setSignTime(currentDate);

 CertificateHolder certHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx",
         getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

 // Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
 // indicating that the signature line contains a signature.
 doc = new Document(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 signatureLine = shape.getSignatureLine();

 Assert.assertTrue(signatureLine.isSigned());
 Assert.assertTrue(signatureLine.isValid());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.util.UUID | Соответствующее значение java.util.UUID. |

### setSignTime(Date value) {#setSignTime-java.util.Date}
```
public void setSignTime(Date value)
```


Дата подписи. Значение по умолчанию — **current time**.

 **Examples:** 

Показывает, как цифрово подписывать документы.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment and date which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("My comment");
     signOptions.setSignTime(new Date());
 }

 // Take an unsigned document from the local file system via a file stream,
 // then create a signed copy of it determined by the filename of the output file stream.
 InputStream streamIn = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream streamOut = new FileOutputStream(getArtifactsDir() + "DigitalSignatureUtil.SignDocument.docx");
     try {
         DigitalSignatureUtil.sign(streamIn, streamOut, certificateHolder, signOptions);
     } finally {
         if (streamOut != null) streamOut.close();
     }
 } finally {
     if (streamIn != null) streamIn.close();
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.util.Date | Соответствующее значение java.util.Date. |

### setSignatureLineId(UUID value) {#setSignatureLineId-java.util.UUID}
```
public void setSignatureLineId(UUID value)
```


Идентификатор строки подписи. Значение по умолчанию — **Empty (all zeroes) Guid**.

 **Remarks:** 

При установке он связывает [SignatureLine](../../com.aspose.words/signatureline/) с соответствующей [DigitalSignature](../../com.aspose.words/digitalsignature/).

 **Examples:** 

Показывает, как добавить строку подписи в документ, а затем подписать его с помощью цифрового сертификата.

```

 public static void sign() throws Exception {
     String signPersonName = "Ron Williams";
     String srcDocumentPath = getMyDir() + "Document.docx";
     String dstDocumentPath = getArtifactsDir() + "SignDocumentCustom.Sign.docx";
     String certificatePath = getMyDir() + "morzal.pfx";
     String certificatePassword = "aw";

     // We need to create simple list with test signers for this example.
     createSignPersonData();
     System.out.println("Test data successfully added!");

     // Get sign person object by name of the person who must sign a document.
     // This an example, in real use case you would return an object from a database.
     SignPersonTestClass signPersonInfo = gSignPersonList.stream().filter(x -> x.getName() == signPersonName).findFirst().get();

     if (signPersonInfo != null) {
         signDocument(srcDocumentPath, dstDocumentPath, signPersonInfo, certificatePath, certificatePassword);
         System.out.println("Document successfully signed!");
     } else {
         System.out.println("Sign person does not exist, please check your parameters.");
     }

     // Now do something with a signed document, for example, save it to your database.
     // Use 'new Document(dstDocumentPath)' for loading a signed document.
 }

 /// 
 /// Signs the document obtained at the source location and saves it to the specified destination.
 /// 
 private static void signDocument(final String srcDocumentPath, final String dstDocumentPath,
                                  final SignPersonTestClass signPersonInfo, final String certificatePath,
                                  final String certificatePassword) throws Exception {
     // Create new document instance based on a test file that we need to sign.
     Document document = new Document(srcDocumentPath);
     DocumentBuilder builder = new DocumentBuilder(document);

     // Add info about responsible person who sign a document.
     SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
     signatureLineOptions.setSigner(signPersonInfo.getName());
     signatureLineOptions.setSignerTitle(signPersonInfo.getPosition());

     // Add signature line for responsible person who sign a document.
     SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
     signatureLine.setId(signPersonInfo.getPersonId());

     // Save a document with line signatures into temporary file for future signing.
     builder.getDocument().save(dstDocumentPath);

     // Create holder of certificate instance based on your personal certificate.
     // This is the test certificate generated for this example.
     CertificateHolder certificateHolder = CertificateHolder.create(certificatePath, certificatePassword);

     // Link our signature line with personal signature.
     SignOptions signOptions = new SignOptions();
     signOptions.setSignatureLineId(signPersonInfo.getPersonId());
     signOptions.setSignatureLineImage(signPersonInfo.getImage());

     // Sign a document which contains signature line with personal certificate.
     DigitalSignatureUtil.sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
 }

 /// 
 /// Create test data that contains info about sing persons.
 /// 
 private static void createSignPersonData() throws IOException {
     InputStream inputStream = new FileInputStream(getImageDir() + "Logo.jpg");

     gSignPersonList = new ArrayList<>();
     gSignPersonList.add(new SignPersonTestClass(UUID.randomUUID(), "Ron Williams", "Chief Executive Officer",
             DocumentHelper.getBytesFromStream(inputStream)));
     gSignPersonList.add(new SignPersonTestClass(UUID.randomUUID(), "Stephen Morse", "Head of Compliance",
             DocumentHelper.getBytesFromStream(inputStream)));
 }

 private static ArrayList gSignPersonList;
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.util.UUID | Соответствующее значение java.util.UUID. |

### setSignatureLineImage(byte[] value) {#setSignatureLineImage-byte}
```
public void setSignatureLineImage(byte[] value)
```


Изображение, которое будет отображаться в связанной [SignatureLine](../../com.aspose.words/signatureline/). Значение по умолчанию — null.

 **Examples:** 

Показывает, как добавить строку подписи в документ, а затем подписать его с помощью цифрового сертификата.

```

 public static void sign() throws Exception {
     String signPersonName = "Ron Williams";
     String srcDocumentPath = getMyDir() + "Document.docx";
     String dstDocumentPath = getArtifactsDir() + "SignDocumentCustom.Sign.docx";
     String certificatePath = getMyDir() + "morzal.pfx";
     String certificatePassword = "aw";

     // We need to create simple list with test signers for this example.
     createSignPersonData();
     System.out.println("Test data successfully added!");

     // Get sign person object by name of the person who must sign a document.
     // This an example, in real use case you would return an object from a database.
     SignPersonTestClass signPersonInfo = gSignPersonList.stream().filter(x -> x.getName() == signPersonName).findFirst().get();

     if (signPersonInfo != null) {
         signDocument(srcDocumentPath, dstDocumentPath, signPersonInfo, certificatePath, certificatePassword);
         System.out.println("Document successfully signed!");
     } else {
         System.out.println("Sign person does not exist, please check your parameters.");
     }

     // Now do something with a signed document, for example, save it to your database.
     // Use 'new Document(dstDocumentPath)' for loading a signed document.
 }

 /// 
 /// Signs the document obtained at the source location and saves it to the specified destination.
 /// 
 private static void signDocument(final String srcDocumentPath, final String dstDocumentPath,
                                  final SignPersonTestClass signPersonInfo, final String certificatePath,
                                  final String certificatePassword) throws Exception {
     // Create new document instance based on a test file that we need to sign.
     Document document = new Document(srcDocumentPath);
     DocumentBuilder builder = new DocumentBuilder(document);

     // Add info about responsible person who sign a document.
     SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
     signatureLineOptions.setSigner(signPersonInfo.getName());
     signatureLineOptions.setSignerTitle(signPersonInfo.getPosition());

     // Add signature line for responsible person who sign a document.
     SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
     signatureLine.setId(signPersonInfo.getPersonId());

     // Save a document with line signatures into temporary file for future signing.
     builder.getDocument().save(dstDocumentPath);

     // Create holder of certificate instance based on your personal certificate.
     // This is the test certificate generated for this example.
     CertificateHolder certificateHolder = CertificateHolder.create(certificatePath, certificatePassword);

     // Link our signature line with personal signature.
     SignOptions signOptions = new SignOptions();
     signOptions.setSignatureLineId(signPersonInfo.getPersonId());
     signOptions.setSignatureLineImage(signPersonInfo.getImage());

     // Sign a document which contains signature line with personal certificate.
     DigitalSignatureUtil.sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
 }

 /// 
 /// Create test data that contains info about sing persons.
 /// 
 private static void createSignPersonData() throws IOException {
     InputStream inputStream = new FileInputStream(getImageDir() + "Logo.jpg");

     gSignPersonList = new ArrayList<>();
     gSignPersonList.add(new SignPersonTestClass(UUID.randomUUID(), "Ron Williams", "Chief Executive Officer",
             DocumentHelper.getBytesFromStream(inputStream)));
     gSignPersonList.add(new SignPersonTestClass(UUID.randomUUID(), "Stephen Morse", "Head of Compliance",
             DocumentHelper.getBytesFromStream(inputStream)));
 }

 private static ArrayList gSignPersonList;
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | byte[] | Соответствующее значение byte[]. |

### setVerticalResolution(int value) {#setVerticalResolution-int}
```
public void setVerticalResolution(int value)
```


Устанавливает вертикальное разрешение для цифровой подписи. Значение по умолчанию — 1200.

 **Examples:** 

Показывает, как подписать документ с дополнительными параметрами подписи.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setWindowsVersion("10.0");
     signOptions.setApplicationVersion("16.0.19127");
     signOptions.setOfficeVersion("16.0.19127/27");
     signOptions.setHorizontalResolution(1024);
     signOptions.setVerticalResolution(768);
     signOptions.setColorDepth(24);
 }

 byte[] certBytes = Files.readAllBytes(Paths.get(getMyDir() + "morzal.pfx"));
 CertificateHolder cert = CertificateHolder.create(certBytes, "aw");
 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.docx");

 DigitalSignature signature = signedDoc.getDigitalSignatures().get(0);
 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signature.isValid());
 Assert.assertEquals("10.0", signature.getWindowsVersion());
 Assert.assertEquals("16.0.19127", signature.getApplicationVersion());
 Assert.assertEquals("16.0.19127/27", signature.getOfficeVersion());
 Assert.assertEquals(1024, signature.getHorizontalResolution());
 Assert.assertEquals(768, signature.getVerticalResolution());
 Assert.assertEquals(24, signature.getColorDepth());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Вертикальное разрешение для цифровой подписи. |

### setWindowsVersion(String value) {#setWindowsVersion-java.lang.String}
```
public void setWindowsVersion(String value)
```


Устанавливает версию Windows для цифровой подписи. Значение по умолчанию — "6.1".

 **Examples:** 

Показывает, как подписать документ с дополнительными параметрами подписи.

```

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setWindowsVersion("10.0");
     signOptions.setApplicationVersion("16.0.19127");
     signOptions.setOfficeVersion("16.0.19127/27");
     signOptions.setHorizontalResolution(1024);
     signOptions.setVerticalResolution(768);
     signOptions.setColorDepth(24);
 }

 byte[] certBytes = Files.readAllBytes(Paths.get(getMyDir() + "morzal.pfx"));
 CertificateHolder cert = CertificateHolder.create(certBytes, "aw");
 DigitalSignatureUtil.sign(getMyDir() + "Digitally signed.docx", getArtifactsDir() + "DigitalSignatureUtil.docx", cert, signOptions);

 Document signedDoc = new Document(getArtifactsDir() + "DigitalSignatureUtil.docx");

 DigitalSignature signature = signedDoc.getDigitalSignatures().get(0);
 Assert.assertEquals(1, signedDoc.getDigitalSignatures().getCount());
 Assert.assertTrue(signature.isValid());
 Assert.assertEquals("10.0", signature.getWindowsVersion());
 Assert.assertEquals("16.0.19127", signature.getApplicationVersion());
 Assert.assertEquals("16.0.19127/27", signature.getOfficeVersion());
 Assert.assertEquals(1024, signature.getHorizontalResolution());
 Assert.assertEquals(768, signature.getVerticalResolution());
 Assert.assertEquals(24, signature.getColorDepth());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Версия Windows для цифровой подписи. |

### setXmlDsigLevel(int value) {#setXmlDsigLevel-int}
```
public void setXmlDsigLevel(int value)
```


Указывает уровень цифровой подписи на основе стандарта XML-DSig. Значение по умолчанию — [XmlDsigLevel.XML\_D\_SIG](../../com.aspose.words/xmldsiglevel/\#XML-D-SIG).

 **Remarks:** 

Различные уровни подписей XAdES могут быть созданы, начиная с Office 2010.

 **Examples:** 

Показывает, как подписать документ на основе стандарта XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее  int  значение. Значение должно быть одним из констант [XmlDsigLevel](../../com.aspose.words/xmldsiglevel/). |

