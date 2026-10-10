---
title: "SignatureLine"
linktitle: "SignatureLine"
second_title: "Aspose.Words Java için"
description: "Java'da imza satırı özelliklerine erişim sağlar."
type: docs
weight: 621
url: /tr/java/com.aspose.words/signatureline/
---

**Inheritance:**
java.lang.Object
```
public class SignatureLine
```

İmza satırı özelliklerine erişim sağlar.

Daha fazla bilgi için, [ Work with Digital Signatures ][Work with Digital Signatures] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```


[Work with Digital Signatures]: https://docs.aspose.com/words/java/working-with-digital-signatures/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAllowComments()](#getAllowComments) | İmzalayanın İmzala iletişim kutusunda yorum ekleyebileceğini gösteren bir değer alır. |
| [getDefaultInstructions()](#getDefaultInstructions) | İşaretleme iletişim kutusunda varsayılan talimatların gösterildiğini belirten bir değeri alır. |
| [getEmail()](#getEmail) | Önerilen imzalayanın e-posta adresini alır. |
| [getId()](#getId) | Bu imza satırı için tanımlayıcıyı alır. |
| [getInstructions()](#getInstructions) | İmza satırını imzalarken gösterilen imzalayana talimatları alır. |
| [getProviderId()](#getProviderId) | Bu imza satırı için imza sağlayıcı tanımlayıcısını alır. |
| [getShowDate()](#getShowDate) | İmza satırında imza tarihinin gösterildiğini belirten bir değeri alır. |
| [getSigner()](#getSigner) | İmza satırının önerilen imzalayanını alır. |
| [getSignerTitle()](#getSignerTitle) | Önerilen imzalayanın unvanını alır (örneğin, Yönetici). |
| [isSigned()](#isSigned) | İmza satırının dijital imza ile imzalandığını gösterir. |
| [isValid()](#isValid) | İmza satırının dijital imza ile imzalandığını ve bu dijital imzanın geçerli olduğunu gösterir. |
| [setAllowComments(boolean value)](#setAllowComments-boolean) | İmzalayanın İşaretleme iletişim kutusunda yorum ekleyebileceğini belirten bir değeri ayarlar. |
| [setDefaultInstructions(boolean value)](#setDefaultInstructions-boolean) | İşaretleme iletişim kutusunda varsayılan talimatların gösterildiğini belirten bir değeri ayarlar. |
| [setEmail(String value)](#setEmail-java.lang.String) | Önerilen imzalayanın e-posta adresini ayarlar. |
| [setId(UUID value)](#setId-java.util.UUID) | Bu imza satırı için tanımlayıcıyı ayarlar. |
| [setInstructions(String value)](#setInstructions-java.lang.String) | İmza satırını imzalarken gösterilen imzalayana talimatları ayarlar. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID) | Bu imza satırı için imza sağlayıcı tanımlayıcısını ayarlar. |
| [setShowDate(boolean value)](#setShowDate-boolean) | İmza satırında imza tarihinin gösterildiğini belirten bir değeri ayarlar. |
| [setSigner(String value)](#setSigner-java.lang.String) | İmza satırının önerilen imzalayanını ayarlar. |
| [setSignerTitle(String value)](#setSignerTitle-java.lang.String) | Önerilen imzalayanın unvanını ayarlar (örneğin, Yönetici). |
### getAllowComments() {#getAllowComments}
```
public boolean getAllowComments()
```


İmzalayanın İşaretleme iletişim kutusunda yorum ekleyebileceğini belirten bir değeri alır. Bu özelliğin varsayılan değeri false'tur.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
boolean - İmzalayanın İşaretleme iletişim kutusunda yorum ekleyebileceğini belirten bir değer.
### getDefaultInstructions() {#getDefaultInstructions}
```
public boolean getDefaultInstructions()
```


İşaretleme iletişim kutusunda varsayılan talimatların gösterildiğini belirten bir değeri alır. Bu özelliğin varsayılan değeri true'dur.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
boolean - İşaretleme iletişim kutusunda varsayılan talimatların gösterildiğini belirten bir değer.
### getEmail() {#getEmail}
```
public String getEmail()
```


Önerilen imzalayanın e-posta adresini alır. Bu özelliğin varsayılan değeri **empty string**'tir.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
java.lang.String - Önerilen imzalayanın e-posta adresi.
### getId() {#getId}
```
public UUID getId()
```


Bu imza satırı için tanımlayıcıyı alır.

Bu tanımlayıcı, belgeyi [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil/) kullanarak imzalarken bir dijital imza ile ilişkilendirilebilir. Bu değer benzersiz olmalıdır ve varsayılan olarak rastgele oluşturulan yeni bir Guid'dir.

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
java.util.UUID - Bu imza satırı için tanımlayıcı.
### getInstructions() {#getInstructions}
```
public String getInstructions()
```


İmza satırı imzalanırken imzacıya gösterilen talimatları alır. Bu özellik, [getDefaultInstructions()](../../com.aspose.words/signatureline/\#getDefaultInstructions) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline/\#setDefaultInstructions-boolean) ayarlanmışsa yok sayılır. Bu özelliğin varsayılan değeri **empty string**.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
java.lang.String - İmza satırını imzalarken gösterilen imzalayana talimatlar.
### getProviderId() {#getProviderId}
```
public UUID getProviderId()
```


Bu imza satırı için imza sağlayıcı tanımlayıcısını alır. Varsayılan değer "\{00000000-0000-0000-0000-000000000000\}".

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
java.util.UUID - Bu imza satırı için imza sağlayıcı tanımlayıcısı.
### getShowDate() {#getShowDate}
```
public boolean getShowDate()
```


İmza satırında imza tarihinin gösterildiğini belirten bir değeri alır. Bu özelliğin varsayılan değeri true'dur.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
boolean - İmza satırında imza tarihinin gösterildiğini belirten bir değer.
### getSigner() {#getSigner}
```
public String getSigner()
```


İmza satırının önerilen imzalayanını alır. Bu özelliğin varsayılan değeri **empty string**'tir.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
java.lang.String - İmza satırının önerilen imzalayanı.
### getSignerTitle() {#getSignerTitle}
```
public String getSignerTitle()
```


Önerilen imzacı unvanını alır (örneğin, Yönetici). Bu özelliğin varsayılan değeri **empty string**.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Returns:**
java.lang.String - Önerilen imzacı unvanı (örneğin, Yönetici).
### isSigned() {#isSigned}
```
public boolean isSigned()
```


İmza satırının dijital imza ile imzalandığını gösterir.

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
boolean - İlgili  boolean  değeri.
### isValid() {#isValid}
```
public boolean isValid()
```


İmza satırının dijital imza ile imzalandığını ve bu dijital imzanın geçerli olduğunu gösterir.

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
boolean - İlgili  boolean  değeri.
### setAllowComments(boolean value) {#setAllowComments-boolean}
```
public void setAllowComments(boolean value)
```


İmzalayanın İmzala iletişim kutusunda yorum ekleyebileceğini gösteren bir değer ayarlar. Bu özelliğin varsayılan değeri false.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İmzalayanın İmzala iletişim kutusunda yorum ekleyebileceğini gösteren bir değer. |

### setDefaultInstructions(boolean value) {#setDefaultInstructions-boolean}
```
public void setDefaultInstructions(boolean value)
```


Varsayılan talimatların İmzala iletişim kutusunda gösterildiğini belirten bir değer ayarlar. Bu özelliğin varsayılan değeri true.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Varsayılan talimatların İmzala iletişim kutusunda gösterildiğini belirten bir değer. |

### setEmail(String value) {#setEmail-java.lang.String}
```
public void setEmail(String value)
```


Önerilen imzalayanın e-posta adresini ayarlar. Bu özelliğin varsayılan değeri **empty string**.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Önerilen imzalayanın e-posta adresi. |

### setId(UUID value) {#setId-java.util.UUID}
```
public void setId(UUID value)
```


Bu imza satırı için tanımlayıcıyı ayarlar.

Bu tanımlayıcı, belgeyi [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil/) kullanarak imzalarken bir dijital imza ile ilişkilendirilebilir. Bu değer benzersiz olmalıdır ve varsayılan olarak rastgele oluşturulan yeni bir Guid'dir.

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
| değer | java.util.UUID | Bu imza satırı için tanımlayıcı. |

### setInstructions(String value) {#setInstructions-java.lang.String}
```
public void setInstructions(String value)
```


İmza satırı imzalanırken imzacıya gösterilen talimatları ayarlar. Bu özellik, [getDefaultInstructions()](../../com.aspose.words/signatureline/\#getDefaultInstructions) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline/\#setDefaultInstructions-boolean) ayarlanmışsa yok sayılır. Bu özelliğin varsayılan değeri **empty string**.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İmzalama satırını imzalarken imzalayana gösterilen talimatlar. |

### setProviderId(UUID value) {#setProviderId-java.util.UUID}
```
public void setProviderId(UUID value)
```


Bu imza satırı için imza sağlayıcı tanımlayıcısını ayarlar. Varsayılan değer "\{00000000-0000-0000-0000-000000000000\}".

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
| değer | java.util.UUID | Bu imza satırı için imza sağlayıcı tanımlayıcısı. |

### setShowDate(boolean value) {#setShowDate-boolean}
```
public void setShowDate(boolean value)
```


İmza tarihinin imzalama satırında gösterildiğini belirten bir değer ayarlar. Bu özelliğin varsayılan değeri true.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İmza tarihinin imzalama satırında gösterildiğini belirten bir değer. |

### setSigner(String value) {#setSigner-java.lang.String}
```
public void setSigner(String value)
```


İmzalama satırının önerilen imzalayanını ayarlar. Bu özelliğin varsayılan değeri **empty string**.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İmzalama satırının önerilen imzalayanı. |

### setSignerTitle(String value) {#setSignerTitle-java.lang.String}
```
public void setSignerTitle(String value)
```


Önerilen imzacı unvanını ayarlar (örneğin, Yönetici). Bu özelliğin varsayılan değeri **empty string**.

 **Examples:** 

Bir imza için satır oluşturmanın ve belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions options = new SignatureLineOptions();
 {
     options.setAllowComments(true);
     options.setDefaultInstructions(true);
     options.setEmail("john.doe@management.com");
     options.setInstructions("Please sign here");
     options.setShowDate(true);
     options.setSigner("John Doe");
     options.setSignerTitle("Senior Manager");
 }

 // Insert a shape that will contain a signature line, whose appearance we will
 // customize using the "SignatureLineOptions" object we have created above.
 // If we insert a shape whose coordinates originate at the bottom right hand corner of the page,
 // we will need to supply negative x and y coordinates to bring the shape into view.
 Shape shape = builder.insertSignatureLine(options, RelativeHorizontalPosition.RIGHT_MARGIN, -170.0,
         RelativeVerticalPosition.BOTTOM_MARGIN, -60.0, WrapType.NONE);

 Assert.assertTrue(shape.isSignatureLine());

 // Verify the properties of our signature line via its Shape object.
 SignatureLine signatureLine = shape.getSignatureLine();

 Assert.assertEquals(signatureLine.getEmail(), "john.doe@management.com");
 Assert.assertEquals(signatureLine.getSigner(), "John Doe");
 Assert.assertEquals(signatureLine.getSignerTitle(), "Senior Manager");
 Assert.assertEquals(signatureLine.getInstructions(), "Please sign here");
 Assert.assertTrue(signatureLine.getShowDate());
 Assert.assertTrue(signatureLine.getAllowComments());
 Assert.assertTrue(signatureLine.getDefaultInstructions());

 doc.save(getArtifactsDir() + "Shape.SignatureLine.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Önerilen imzacı unvanı (örneğin, Yönetici). |

