---
title: "SignOptions"
linktitle: "SignOptions"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier les options de signature de document en Java."
type: docs
weight: 620
url: /fr/java/com.aspose.words/signoptions/
---

**Inheritance:**
java.lang.Object
```
public class SignOptions
```

Permet de spécifier les options pour la signature de documents.

Pour en savoir plus, consultez l'article de documentation [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

Montre comment signer numériquement des documents.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getApplicationVersion()](#getApplicationVersion) | Obtient la version de l'application pour la signature numérique. |
| [getColorDepth()](#getColorDepth) | Obtient la profondeur de couleur pour la signature numérique. |
| [getComments()](#getComments) | Spécifie les commentaires sur la signature numérique. |
| [getDecryptionPassword()](#getDecryptionPassword) | Le mot de passe pour déchiffrer le document source. |
| [getHorizontalResolution()](#getHorizontalResolution) | Obtient la résolution horizontale de la signature numérique. |
| [getOfficeVersion()](#getOfficeVersion) | Obtient la version Office de la signature numérique. |
| [getProviderId()](#getProviderId) | Spécifie l'ID de classe du fournisseur de signature. |
| [getSignTime()](#getSignTime) | La date de la signature. |
| [getSignatureLineId()](#getSignatureLineId) | Identifiant de la ligne de signature. |
| [getSignatureLineImage()](#getSignatureLineImage) | L'image qui sera affichée dans le [SignatureLine](../../com.aspose.words/signatureline/) associé. |
| [getVerticalResolution()](#getVerticalResolution) | Obtient la résolution verticale de la signature numérique. |
| [getWindowsVersion()](#getWindowsVersion) | Obtient la version Windows de la signature numérique. |
| [getXmlDsigLevel()](#getXmlDsigLevel) | Spécifie le niveau d'une signature numérique basé sur la norme XML-DSig. |
| [setApplicationVersion(String value)](#setApplicationVersion-java.lang.String) | Définit la version de l'application pour la signature numérique. |
| [setColorDepth(int value)](#setColorDepth-int) | Définit la profondeur de couleur de la signature numérique. |
| [setComments(String value)](#setComments-java.lang.String) | Spécifie les commentaires sur la signature numérique. |
| [setDecryptionPassword(String value)](#setDecryptionPassword-java.lang.String) | Le mot de passe pour déchiffrer le document source. |
| [setHorizontalResolution(int value)](#setHorizontalResolution-int) | Définit la résolution horizontale de la signature numérique. |
| [setOfficeVersion(String value)](#setOfficeVersion-java.lang.String) | Définit la version Office de la signature numérique. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID) | Spécifie l'ID de classe du fournisseur de signature. |
| [setSignTime(Date value)](#setSignTime-java.util.Date) | La date de la signature. |
| [setSignatureLineId(UUID value)](#setSignatureLineId-java.util.UUID) | Identifiant de la ligne de signature. |
| [setSignatureLineImage(byte[] value)](#setSignatureLineImage-byte) | L'image qui sera affichée dans le [SignatureLine](../../com.aspose.words/signatureline/) associé. |
| [setVerticalResolution(int value)](#setVerticalResolution-int) | Définit la résolution verticale de la signature numérique. |
| [setWindowsVersion(String value)](#setWindowsVersion-java.lang.String) | Définit la version Windows de la signature numérique. |
| [setXmlDsigLevel(int value)](#setXmlDsigLevel-int) | Spécifie le niveau d'une signature numérique basé sur la norme XML-DSig. |
### getApplicationVersion() {#getApplicationVersion}
```
public String getApplicationVersion()
```


Obtient la version de l'application pour la signature numérique. La valeur par défaut est "12.0".

 **Examples:** 

Montre comment signer un document avec des options de signature supplémentaires.

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
java.lang.String - La version de l'application pour la signature numérique.
### getColorDepth() {#getColorDepth}
```
public int getColorDepth()
```


Obtient la profondeur de couleur de la signature numérique. La valeur par défaut est 32.

 **Examples:** 

Montre comment signer un document avec des options de signature supplémentaires.

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
int - La profondeur de couleur de la signature numérique.
### getComments() {#getComments}
```
public String getComments()
```


Spécifie les commentaires sur la signature numérique. La valeur par défaut est **empty string**.

 **Examples:** 

Montre comment signer numériquement des documents.

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
java.lang.String - La valeur java.lang.String correspondante.
### getDecryptionPassword() {#getDecryptionPassword}
```
public String getDecryptionPassword()
```


Le mot de passe pour déchiffrer le document source. La valeur par défaut est **empty string**.

 **Remarks:** 

Si le document OOXML est chiffré, vous devez fournir le mot de passe de déchiffrement pour déchiffrer le document source avant qu'il ne soit signé. Cela n'est pas requis pour les documents au format binaire DOC.

 **Examples:** 

Montre comment signer un fichier de document chiffré.

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
java.lang.String - La valeur java.lang.String correspondante.
### getHorizontalResolution() {#getHorizontalResolution}
```
public int getHorizontalResolution()
```


Obtient la résolution horizontale de la signature numérique. La valeur par défaut est 1920.

 **Examples:** 

Montre comment signer un document avec des options de signature supplémentaires.

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
int - La résolution horizontale de la signature numérique.
### getOfficeVersion() {#getOfficeVersion}
```
public String getOfficeVersion()
```


Obtient la version Office pour la signature numérique. La valeur par défaut est "12.0".

 **Examples:** 

Montre comment signer un document avec des options de signature supplémentaires.

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
java.lang.String - La version Office pour la signature numérique.
### getProviderId() {#getProviderId}
```
public UUID getProviderId()
```


Spécifie l'ID de classe du fournisseur de signature. La valeur par défaut est **Empty (all zeroes) Guid**.

 **Remarks:** 

Le fournisseur de services cryptographiques (CSP) est un module logiciel indépendant qui exécute réellement les algorithmes de cryptographie pour l'authentification, le codage et le chiffrement. MS Office réserve la valeur de \\{00000000-0000-0000-0000-000000000000\\} pour son fournisseur de signature par défaut.

Le GUID du fournisseur installé supplémentaire doit être obtenu à partir de la documentation fournie avec le fournisseur.

De plus, tous les fournisseurs cryptographiques installés sont répertoriés dans le registre Windows. Ils se trouvent dans le chemin suivant : HKLM\\\\SOFTWARE\\\\Microsoft\\\\Cryptography\\\\Defaults\\\\Provider. Il existe une clé nommée "CP Service UUID" qui correspond à un GUID du fournisseur de signature.

 **Examples:** 

Montre comment signer un document avec un certificat personnel et une ligne de signature.

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
java.util.UUID - La valeur java.util.UUID correspondante.
### getSignTime() {#getSignTime}
```
public Date getSignTime()
```


La date de signature. La valeur par défaut est **current time**

 **Examples:** 

Montre comment signer numériquement des documents.

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
java.util.Date - La valeur java.util.Date correspondante.
### getSignatureLineId() {#getSignatureLineId}
```
public UUID getSignatureLineId()
```


Identifiant de la ligne de signature. La valeur par défaut est **Empty (all zeroes) Guid**.

 **Remarks:** 

Lorsqu'il est défini, il associe [SignatureLine](../../com.aspose.words/signatureline/) à la [DigitalSignature](../../com.aspose.words/digitalsignature/) correspondante.

 **Examples:** 

Montre comment ajouter une ligne de signature à un document, puis la signer à l'aide d'un certificat numérique.

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
java.util.UUID - La valeur java.util.UUID correspondante.
### getSignatureLineImage() {#getSignatureLineImage}
```
public byte[] getSignatureLineImage()
```


L'image qui sera affichée dans la [SignatureLine](../../com.aspose.words/signatureline/) associée. La valeur par défaut est  null .

 **Examples:** 

Montre comment ajouter une ligne de signature à un document, puis la signer à l'aide d'un certificat numérique.

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
byte[] - La valeur byte[] correspondante.
### getVerticalResolution() {#getVerticalResolution}
```
public int getVerticalResolution()
```


Obtient la résolution verticale pour la signature numérique. La valeur par défaut est 1200.

 **Examples:** 

Montre comment signer un document avec des options de signature supplémentaires.

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
int - La résolution verticale pour la signature numérique.
### getWindowsVersion() {#getWindowsVersion}
```
public String getWindowsVersion()
```


Obtient la version Windows pour la signature numérique. La valeur par défaut est "6.1".

 **Examples:** 

Montre comment signer un document avec des options de signature supplémentaires.

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
java.lang.String - La version Windows pour la signature numérique.
### getXmlDsigLevel() {#getXmlDsigLevel}
```
public int getXmlDsigLevel()
```


Spécifie le niveau d'une signature numérique basé sur la norme XML-DSig. La valeur par défaut est [XmlDsigLevel.XML\\_D\\_SIG](../../com.aspose.words/xmldsiglevel/\\#XML-D-SIG).

 **Remarks:** 

Différents niveaux de signatures XAdES peuvent être créés à partir d'Office 2010.

 **Examples:** 

Montre comment signer un document basé sur la norme XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Returns:**
int - La valeur  int  correspondante. La valeur renvoyée est l'une des constantes [XmlDsigLevel](../../com.aspose.words/xmldsiglevel/).
### setApplicationVersion(String value) {#setApplicationVersion-java.lang.String}
```
public void setApplicationVersion(String value)
```


Définit la version de l'application pour la signature numérique. La valeur par défaut est "12.0".

 **Examples:** 

Montre comment signer un document avec des options de signature supplémentaires.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La version de l'application pour la signature numérique. |

### setColorDepth(int value) {#setColorDepth-int}
```
public void setColorDepth(int value)
```


Définit la profondeur de couleur pour la signature numérique. La valeur par défaut est 32.

 **Examples:** 

Montre comment signer un document avec des options de signature supplémentaires.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La profondeur de couleur pour la signature numérique. |

### setComments(String value) {#setComments-java.lang.String}
```
public void setComments(String value)
```


Spécifie les commentaires sur la signature numérique. La valeur par défaut est **empty string**.

 **Examples:** 

Montre comment signer numériquement des documents.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setDecryptionPassword(String value) {#setDecryptionPassword-java.lang.String}
```
public void setDecryptionPassword(String value)
```


Le mot de passe pour déchiffrer le document source. La valeur par défaut est **empty string**.

 **Remarks:** 

Si le document OOXML est chiffré, vous devez fournir le mot de passe de déchiffrement pour déchiffrer le document source avant qu'il ne soit signé. Cela n'est pas requis pour les documents au format binaire DOC.

 **Examples:** 

Montre comment signer un fichier de document chiffré.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setHorizontalResolution(int value) {#setHorizontalResolution-int}
```
public void setHorizontalResolution(int value)
```


Définit la résolution horizontale pour la signature numérique. La valeur par défaut est 1920.

 **Examples:** 

Montre comment signer un document avec des options de signature supplémentaires.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La résolution horizontale pour la signature numérique. |

### setOfficeVersion(String value) {#setOfficeVersion-java.lang.String}
```
public void setOfficeVersion(String value)
```


Définit la version d'Office pour la signature numérique. La valeur par défaut est "12.0".

 **Examples:** 

Montre comment signer un document avec des options de signature supplémentaires.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La version d'Office pour la signature numérique. |

### setProviderId(UUID value) {#setProviderId-java.util.UUID}
```
public void setProviderId(UUID value)
```


Spécifie l'ID de classe du fournisseur de signature. La valeur par défaut est **Empty (all zeroes) Guid**.

 **Remarks:** 

Le fournisseur de services cryptographiques (CSP) est un module logiciel indépendant qui exécute réellement les algorithmes de cryptographie pour l'authentification, le codage et le chiffrement. MS Office réserve la valeur de \\{00000000-0000-0000-0000-000000000000\\} pour son fournisseur de signature par défaut.

Le GUID du fournisseur installé supplémentaire doit être obtenu à partir de la documentation fournie avec le fournisseur.

De plus, tous les fournisseurs cryptographiques installés sont répertoriés dans le registre Windows. Ils se trouvent dans le chemin suivant : HKLM\\\\SOFTWARE\\\\Microsoft\\\\Cryptography\\\\Defaults\\\\Provider. Il existe une clé nommée "CP Service UUID" qui correspond à un GUID du fournisseur de signature.

 **Examples:** 

Montre comment signer un document avec un certificat personnel et une ligne de signature.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.util.UUID | La valeur java.util.UUID correspondante. |

### setSignTime(Date value) {#setSignTime-java.util.Date}
```
public void setSignTime(Date value)
```


La date de signature. La valeur par défaut est **current time**

 **Examples:** 

Montre comment signer numériquement des documents.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.util.Date | La valeur java.util.Date correspondante. |

### setSignatureLineId(UUID value) {#setSignatureLineId-java.util.UUID}
```
public void setSignatureLineId(UUID value)
```


Identifiant de la ligne de signature. La valeur par défaut est **Empty (all zeroes) Guid**.

 **Remarks:** 

Lorsqu'il est défini, il associe [SignatureLine](../../com.aspose.words/signatureline/) à la [DigitalSignature](../../com.aspose.words/digitalsignature/) correspondante.

 **Examples:** 

Montre comment ajouter une ligne de signature à un document, puis la signer à l'aide d'un certificat numérique.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.util.UUID | La valeur java.util.UUID correspondante. |

### setSignatureLineImage(byte[] value) {#setSignatureLineImage-byte}
```
public void setSignatureLineImage(byte[] value)
```


L'image qui sera affichée dans la [SignatureLine](../../com.aspose.words/signatureline/) associée. La valeur par défaut est  null .

 **Examples:** 

Montre comment ajouter une ligne de signature à un document, puis la signer à l'aide d'un certificat numérique.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | byte[] | La valeur byte[] correspondante. |

### setVerticalResolution(int value) {#setVerticalResolution-int}
```
public void setVerticalResolution(int value)
```


Définit la résolution verticale pour la signature numérique. La valeur par défaut est 1200.

 **Examples:** 

Montre comment signer un document avec des options de signature supplémentaires.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La résolution verticale pour la signature numérique. |

### setWindowsVersion(String value) {#setWindowsVersion-java.lang.String}
```
public void setWindowsVersion(String value)
```


Définit la version de Windows pour la signature numérique. La valeur par défaut est "6.1".

 **Examples:** 

Montre comment signer un document avec des options de signature supplémentaires.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La version de Windows pour la signature numérique. |

### setXmlDsigLevel(int value) {#setXmlDsigLevel-int}
```
public void setXmlDsigLevel(int value)
```


Spécifie le niveau d'une signature numérique basé sur la norme XML-DSig. La valeur par défaut est [XmlDsigLevel.XML\\_D\\_SIG](../../com.aspose.words/xmldsiglevel/\\#XML-D-SIG).

 **Remarks:** 

Différents niveaux de signatures XAdES peuvent être créés à partir d'Office 2010.

 **Examples:** 

Montre comment signer un document basé sur la norme XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [XmlDsigLevel](../../com.aspose.words/xmldsiglevel/). |

