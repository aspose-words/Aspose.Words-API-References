---
title: "CertificateHolder"
linktitle: "CertificateHolder"
second_title: "Aspose.Words Java için"
description: "Java'da X509Certificate2 örneğini tutan bir tutucuyu temsil eder."
type: docs
weight: 64
url: /tr/java/com.aspose.words/certificateholder/
---

**Inheritance:**
java.lang.Object
```
public class CertificateHolder
```

**X509Certificate2** örneğini tutan bir tutucuyu temsil eder.

Daha fazla bilgi için, [ Work with Digital Signatures ][Work with Digital Signatures] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

[CertificateHolder](../../com.aspose.words/certificateholder/) can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails/) instead of obsolete methods with **X509Certificate2** as parameters.

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


[Work with Digital Signatures]: https://docs.aspose.com/words/java/working-with-digital-signatures/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [create(byte[] certBytes, String password)](#create-byte---java.lang.String) | PKCS12 deposunun bayt dizisini ve şifresini kullanarak [CertificateHolder](../../com.aspose.words/certificateholder/) nesnesi oluşturur. |
| [create(String fileName, String password)](#create-java.lang.String-java.lang.String) | PKCS12 deposunun yolunu ve şifresini kullanarak [CertificateHolder](../../com.aspose.words/certificateholder/) nesnesi oluşturur. |
| [create(String fileName, String password, String alias)](#create-java.lang.String-java.lang.String-java.lang.String) | PKCS12 deposunun yolunu, şifresini ve özel anahtar ile sertifikanın bulunacağı takma adı kullanarak [CertificateHolder](../../com.aspose.words/certificateholder/) nesnesi oluşturur. |
| [getCertificate()](#getCertificate) | Özel ve genel anahtarları ve sertifika zincirini tutan **X509Certificate2**'yi içeren **X509Certificate2Wrapper** örneğini döndürür. |
### create(byte[] certBytes, String password) {#create-byte---java.lang.String}
```
public static CertificateHolder create(byte[] certBytes, String password)
```


PKCS12 deposunun bayt dizisini ve şifresini kullanarak [CertificateHolder](../../com.aspose.words/certificateholder/) nesnesi oluşturur. **T:Org.BouncyCastle.Security.InvalidParameterException** certBytes null ise fırlatılır **T:Org.BouncyCastle.Security.InvalidParameterException** password null ise fırlatılır

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| certBytes | byte[] | Bir X.509 sertifikasından gelen verileri içeren bayt dizisi. |
| şifre | java.lang.String | X.509 sertifika verilerine erişmek için gerekli şifre. |

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - An instance of [CertificateHolder](../../com.aspose.words/certificateholder/)
### create(String fileName, String password) {#create-java.lang.String-java.lang.String}
```
public static CertificateHolder create(String fileName, String password)
```


PKCS12 deposunun yolunu ve şifresini kullanarak [CertificateHolder](../../com.aspose.words/certificateholder/) nesnesi oluşturur. **T:Org.BouncyCastle.Security.InvalidParameterException** fileName null ise fırlatılır **T:Org.BouncyCastle.Security.InvalidParameterException** password null ise fırlatılır

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Bir sertifika dosyasının adı. |
| şifre | java.lang.String | X.509 sertifika verilerine erişmek için gerekli şifre. |

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - An instance of [CertificateHolder](../../com.aspose.words/certificateholder/)
### create(String fileName, String password, String alias) {#create-java.lang.String-java.lang.String-java.lang.String}
```
public static CertificateHolder create(String fileName, String password, String alias)
```


PKCS12 deposunun yolunu, şifresini ve özel anahtar ile sertifikanın bulunacağı takma adı kullanarak [CertificateHolder](../../com.aspose.words/certificateholder/) nesnesi oluşturur. **T:Org.BouncyCastle.Security.InvalidParameterException** fileName null ise fırlatılır **T:Org.BouncyCastle.Security.InvalidParameterException** password null ise fırlatılır

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Bir sertifika dosyasının adı. |
| şifre | java.lang.String | X.509 sertifika verilerine erişmek için gerekli şifre. |
| alias | java.lang.String | Bir sertifika ve onun özel anahtarı için ilişkili takma ad |

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - An instance of [CertificateHolder](../../com.aspose.words/certificateholder/)
### getCertificate() {#getCertificate}
```
public X509Certificate2Wrapper getCertificate()
```


Özel ve genel anahtarları ve sertifika zincirini tutan **X509Certificate2**'yi içeren **X509Certificate2Wrapper** örneğini döndürür.

 **Examples:** 

Bir belgede her imzanın nasıl doğrulanacağını ve bilgilerin nasıl görüntüleneceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature signature : doc.getDigitalSignatures()) {
     System.out.println("*** Signature Found ***");
     System.out.println("Is valid: " + signature.isValid());
     // This property is available in MS Word documents only
     System.out.println("Reason for signing: " + signature.getComments());
     System.out.println("Signature type: " + signature.getSignatureType());
     System.out.println("Time of signing: " + signature.getSignTime());
     System.out.println("Subject name: " + signature.getSubjectName());
     System.out.println("Issuer name: " + signature.getIssuerName());
     System.out.println();
 }
 
```

**Returns:**
[X509Certificate2Wrapper](../../com.aspose.words/x509certificate2wrapper/) - [X509Certificate2Wrapper](../../com.aspose.words/x509certificate2wrapper/) instance
