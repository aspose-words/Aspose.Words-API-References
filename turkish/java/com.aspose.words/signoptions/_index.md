---
title: "SignOptions"
linktitle: "SignOptions"
second_title: "Aspose.Words Java için"
description: "Java'da belge imzalama seçeneklerini belirtmeye izin verir."
type: docs
weight: 620
url: /tr/java/com.aspose.words/signoptions/
---

**Inheritance:**
java.lang.Object
```
public class SignOptions
```

Belge imzalama seçeneklerini belirtmeye izin verir.

Daha fazla bilgi için, [ Work with Digital Signatures ][Work with Digital Signatures] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Belgeleri dijital olarak imzalamanın nasıl yapılacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getApplicationVersion()](#getApplicationVersion) | Dijital imza için uygulama sürümünü alır. |
| [getColorDepth()](#getColorDepth) | Dijital imza için renk derinliğini alır. |
| [getComments()](#getComments) | Dijital imza üzerindeki yorumları belirtir. |
| [getDecryptionPassword()](#getDecryptionPassword) | Kaynak belgeyi çözmek için şifre. |
| [getHorizontalResolution()](#getHorizontalResolution) | Dijital imza için yatay çözünürlüğü alır. |
| [getOfficeVersion()](#getOfficeVersion) | Dijital imza için Office sürümünü alır. |
| [getProviderId()](#getProviderId) | İmza sağlayıcısının sınıf kimliğini belirtir. |
| [getSignTime()](#getSignTime) | İmza tarihi. |
| [getSignatureLineId()](#getSignatureLineId) | İmza satırı tanımlayıcısı. |
| [getSignatureLineImage()](#getSignatureLineImage) | İlgili [SignatureLine](../../com.aspose.words/signatureline/) içinde gösterilecek görüntü. |
| [getVerticalResolution()](#getVerticalResolution) | Dijital imza için dikey çözünürlüğü alır. |
| [getWindowsVersion()](#getWindowsVersion) | Dijital imza için Windows sürümünü alır. |
| [getXmlDsigLevel()](#getXmlDsigLevel) | XML-DSig standardına dayalı bir dijital imzanın seviyesini belirtir. |
| [setApplicationVersion(String value)](#setApplicationVersion-java.lang.String) | Dijital imza için uygulama sürümünü ayarlar. |
| [setColorDepth(int value)](#setColorDepth-int) | Dijital imza için renk derinliğini ayarlar. |
| [setComments(String value)](#setComments-java.lang.String) | Dijital imza üzerindeki yorumları belirtir. |
| [setDecryptionPassword(String value)](#setDecryptionPassword-java.lang.String) | Kaynak belgeyi çözmek için şifre. |
| [setHorizontalResolution(int value)](#setHorizontalResolution-int) | Dijital imza için yatay çözünürlüğü ayarlar. |
| [setOfficeVersion(String value)](#setOfficeVersion-java.lang.String) | Dijital imza için Office sürümünü ayarlar. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID) | İmza sağlayıcısının sınıf kimliğini belirtir. |
| [setSignTime(Date value)](#setSignTime-java.util.Date) | İmza tarihi. |
| [setSignatureLineId(UUID value)](#setSignatureLineId-java.util.UUID) | İmza satırı tanımlayıcısı. |
| [setSignatureLineImage(byte[] value)](#setSignatureLineImage-byte) | İlgili [SignatureLine](../../com.aspose.words/signatureline/) içinde gösterilecek görüntü. |
| [setVerticalResolution(int value)](#setVerticalResolution-int) | Dijital imza için dikey çözünürlüğü ayarlar. |
| [setWindowsVersion(String value)](#setWindowsVersion-java.lang.String) | Dijital imza için Windows sürümünü ayarlar. |
| [setXmlDsigLevel(int value)](#setXmlDsigLevel-int) | XML-DSig standardına dayalı bir dijital imzanın seviyesini belirtir. |
### getApplicationVersion() {#getApplicationVersion}
```
public String getApplicationVersion()
```


Dijital imza için uygulama sürümünü alır. Varsayılan değer "12.0"dır.

 **Examples:** 

Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.

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
java.lang.String - Dijital imza için uygulama sürümü.
### getColorDepth() {#getColorDepth}
```
public int getColorDepth()
```


Dijital imza için renk derinliğini alır. Varsayılan değer 32'dir.

 **Examples:** 

Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.

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
int - Dijital imza için renk derinliği.
### getComments() {#getComments}
```
public String getComments()
```


Dijital imza üzerindeki yorumları belirtir. Varsayılan değer **empty string**.

 **Examples:** 

Belgeleri dijital olarak imzalamanın nasıl yapılacağını gösterir.

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
java.lang.String - İlgili java.lang.String değeri.
### getDecryptionPassword() {#getDecryptionPassword}
```
public String getDecryptionPassword()
```


Kaynak belgeyi çözmek için şifre. Varsayılan değer **empty string**.

 **Remarks:** 

OOXML belge şifreli ise, imzalanmadan önce kaynak belgeyi çözmek için şifre çözme şifresi sağlamalısınız. Bu, ikili DOC formatındaki belgeler için gerekli değildir.

 **Examples:** 

Şifreli belge dosyasını imzalamayı gösterir.

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
java.lang.String - İlgili java.lang.String değeri.
### getHorizontalResolution() {#getHorizontalResolution}
```
public int getHorizontalResolution()
```


Dijital imza için yatay çözünürlüğü alır. Varsayılan değer 1920'dir.

 **Examples:** 

Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.

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
int - Dijital imza için yatay çözünürlük.
### getOfficeVersion() {#getOfficeVersion}
```
public String getOfficeVersion()
```


Dijital imza için Office sürümünü alır. Varsayılan değer "12.0".

 **Examples:** 

Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.

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
java.lang.String - Dijital imza için Office sürümü.
### getProviderId() {#getProviderId}
```
public UUID getProviderId()
```


İmza sağlayıcısının sınıf kimliğini belirtir. Varsayılan değer **Empty (all zeroes) Guid**.

 **Remarks:** 

Kriptografik hizmet sağlayıcısı (CSP), kimlik doğrulama, kodlama ve şifreleme için kriptografi algoritmalarını gerçekte yürüten bağımsız bir yazılım modülüdür. MS Office, varsayılan imza sağlayıcısı için \{00000000-0000-0000-0000-000000000000\} değerini ayırır.

Ek olarak kurulan sağlayıcının GUID'i, sağlayıcıyla birlikte gelen belgelerden elde edilmelidir.

Ek olarak, kurulu tüm kriptografik sağlayıcılar Windows kayıt defterinde listelenir. Aşağıdaki yolda bulunabilir: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. "CP Service UUID" adlı bir anahtar vardır ve bu, imza sağlayıcısının GUID'ine karşılık gelir.

 **Examples:** 

Kişisel bir sertifika ve imza satırıyla bir belgeyi nasıl imzalayacağınızı gösterir.

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
java.util.UUID - İlgili java.util.UUID değeri.
### getSignTime() {#getSignTime}
```
public Date getSignTime()
```


İmza tarihi. Varsayılan değer **current time**

 **Examples:** 

Belgeleri dijital olarak imzalamanın nasıl yapılacağını gösterir.

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
java.util.Date - İlgili java.util.Date değeri.
### getSignatureLineId() {#getSignatureLineId}
```
public UUID getSignatureLineId()
```


İmza satırı tanımlayıcısı. Varsayılan değer **Empty (all zeroes) Guid**.

 **Remarks:** 

Ayarlandığında, [SignatureLine](../../com.aspose.words/signatureline/) öğesini ilgili [DigitalSignature](../../com.aspose.words/digitalsignature/) ile ilişkilendirir.

 **Examples:** 

Bir belgeye imza satırı eklemeyi ve ardından dijital bir sertifika kullanarak imzalamayı gösterir.

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
java.util.UUID - İlgili java.util.UUID değeri.
### getSignatureLineImage() {#getSignatureLineImage}
```
public byte[] getSignatureLineImage()
```


İlgili [SignatureLine](../../com.aspose.words/signatureline/) içinde gösterilecek görüntü. Varsayılan değer null.

 **Examples:** 

Bir belgeye imza satırı eklemeyi ve ardından dijital bir sertifika kullanarak imzalamayı gösterir.

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
byte[] - İlgili byte[] değeri.
### getVerticalResolution() {#getVerticalResolution}
```
public int getVerticalResolution()
```


Dijital imza için dikey çözünürlüğü alır. Varsayılan değer 1200.

 **Examples:** 

Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.

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
int - Dijital imza için dikey çözünürlük.
### getWindowsVersion() {#getWindowsVersion}
```
public String getWindowsVersion()
```


Dijital imza için Windows sürümünü alır. Varsayılan değer "6.1".

 **Examples:** 

Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.

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
java.lang.String - Dijital imza için Windows sürümü.
### getXmlDsigLevel() {#getXmlDsigLevel}
```
public int getXmlDsigLevel()
```


XML-DSig standardına dayalı bir dijital imzanın seviyesini belirtir. Varsayılan değer [XmlDsigLevel.XML\_D\_SIG](../../com.aspose.words/xmldsiglevel/\#XML-D-SIG).

 **Remarks:** 

Office 2010'dan itibaren farklı XAdES imza seviyeleri oluşturulabilir.

 **Examples:** 

XML-DSig standardına dayalı belgeyi nasıl imzalayacağınızı gösterir.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Returns:**
int - İlgili  int  değeri. Döndürülen değer [XmlDsigLevel](../../com.aspose.words/xmldsiglevel/) sabitlerinden biridir.
### setApplicationVersion(String value) {#setApplicationVersion-java.lang.String}
```
public void setApplicationVersion(String value)
```


Dijital imza için uygulama sürümünü ayarlar. Varsayılan değer "12.0".

 **Examples:** 

Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Dijital imza için uygulama sürümü. |

### setColorDepth(int value) {#setColorDepth-int}
```
public void setColorDepth(int value)
```


Dijital imza için renk derinliğini ayarlar. Varsayılan değer 32.

 **Examples:** 

Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Dijital imza için renk derinliği. |

### setComments(String value) {#setComments-java.lang.String}
```
public void setComments(String value)
```


Dijital imza üzerindeki yorumları belirtir. Varsayılan değer **empty string**.

 **Examples:** 

Belgeleri dijital olarak imzalamanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setDecryptionPassword(String value) {#setDecryptionPassword-java.lang.String}
```
public void setDecryptionPassword(String value)
```


Kaynak belgeyi çözmek için şifre. Varsayılan değer **empty string**.

 **Remarks:** 

OOXML belge şifreli ise, imzalanmadan önce kaynak belgeyi çözmek için şifre çözme şifresi sağlamalısınız. Bu, ikili DOC formatındaki belgeler için gerekli değildir.

 **Examples:** 

Şifreli belge dosyasını imzalamayı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setHorizontalResolution(int value) {#setHorizontalResolution-int}
```
public void setHorizontalResolution(int value)
```


Dijital imza için yatay çözünürlüğü ayarlar. Varsayılan değer 1920'dir.

 **Examples:** 

Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Dijital imza için yatay çözünürlük. |

### setOfficeVersion(String value) {#setOfficeVersion-java.lang.String}
```
public void setOfficeVersion(String value)
```


Dijital imza için Office sürümünü ayarlar. Varsayılan değer "12.0".

 **Examples:** 

Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Dijital imza için Office sürümü. |

### setProviderId(UUID value) {#setProviderId-java.util.UUID}
```
public void setProviderId(UUID value)
```


İmza sağlayıcısının sınıf kimliğini belirtir. Varsayılan değer **Empty (all zeroes) Guid**.

 **Remarks:** 

Kriptografik hizmet sağlayıcısı (CSP), kimlik doğrulama, kodlama ve şifreleme için kriptografi algoritmalarını gerçekte yürüten bağımsız bir yazılım modülüdür. MS Office, varsayılan imza sağlayıcısı için \{00000000-0000-0000-0000-000000000000\} değerini ayırır.

Ek olarak kurulan sağlayıcının GUID'i, sağlayıcıyla birlikte gelen belgelerden elde edilmelidir.

Ek olarak, kurulu tüm kriptografik sağlayıcılar Windows kayıt defterinde listelenir. Aşağıdaki yolda bulunabilir: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. "CP Service UUID" adlı bir anahtar vardır ve bu, imza sağlayıcısının GUID'ine karşılık gelir.

 **Examples:** 

Kişisel bir sertifika ve imza satırıyla bir belgeyi nasıl imzalayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.util.UUID | İlgili java.util.UUID değeri. |

### setSignTime(Date value) {#setSignTime-java.util.Date}
```
public void setSignTime(Date value)
```


İmza tarihi. Varsayılan değer **current time**

 **Examples:** 

Belgeleri dijital olarak imzalamanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.util.Date | İlgili java.util.Date değeri. |

### setSignatureLineId(UUID value) {#setSignatureLineId-java.util.UUID}
```
public void setSignatureLineId(UUID value)
```


İmza satırı tanımlayıcısı. Varsayılan değer **Empty (all zeroes) Guid**.

 **Remarks:** 

Ayarlandığında, [SignatureLine](../../com.aspose.words/signatureline/) öğesini ilgili [DigitalSignature](../../com.aspose.words/digitalsignature/) ile ilişkilendirir.

 **Examples:** 

Bir belgeye imza satırı eklemeyi ve ardından dijital bir sertifika kullanarak imzalamayı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.util.UUID | İlgili java.util.UUID değeri. |

### setSignatureLineImage(byte[] value) {#setSignatureLineImage-byte}
```
public void setSignatureLineImage(byte[] value)
```


İlgili [SignatureLine](../../com.aspose.words/signatureline/) içinde gösterilecek görüntü. Varsayılan değer null.

 **Examples:** 

Bir belgeye imza satırı eklemeyi ve ardından dijital bir sertifika kullanarak imzalamayı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | byte[] | İlgili byte[] değeri. |

### setVerticalResolution(int value) {#setVerticalResolution-int}
```
public void setVerticalResolution(int value)
```


Dijital imza için dikey çözünürlüğü ayarlar. Varsayılan değer 1200.

 **Examples:** 

Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Dijital imza için dikey çözünürlük. |

### setWindowsVersion(String value) {#setWindowsVersion-java.lang.String}
```
public void setWindowsVersion(String value)
```


Dijital imza için Windows sürümünü ayarlar. Varsayılan değer "6.1".

 **Examples:** 

Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Dijital imza için Windows sürümü. |

### setXmlDsigLevel(int value) {#setXmlDsigLevel-int}
```
public void setXmlDsigLevel(int value)
```


XML-DSig standardına dayalı bir dijital imzanın seviyesini belirtir. Varsayılan değer [XmlDsigLevel.XML\_D\_SIG](../../com.aspose.words/xmldsiglevel/\#XML-D-SIG).

 **Remarks:** 

Office 2010'dan itibaren farklı XAdES imza seviyeleri oluşturulabilir.

 **Examples:** 

XML-DSig standardına dayalı belgeyi nasıl imzalayacağınızı gösterir.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [XmlDsigLevel](../../com.aspose.words/xmldsiglevel/) sabitlerinden biri olmalıdır. |

