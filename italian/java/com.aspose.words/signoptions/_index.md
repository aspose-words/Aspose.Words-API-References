---
title: "SignOptions"
linktitle: "SignOptions"
second_title: "Aspose.Words per Java"
description: "Consente di specificare le opzioni per la firma dei documenti in Java."
type: docs
weight: 620
url: /it/java/com.aspose.words/signoptions/
---

**Inheritance:**
java.lang.Object
```
public class SignOptions
```

Consente di specificare le opzioni per la firma del documento.

Per saperne di più, visita l'articolo di documentazione [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

Mostra come firmare digitalmente i documenti.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getApplicationVersion()](#getApplicationVersion) | Ottiene la versione dell'applicazione per la firma digitale. |
| [getColorDepth()](#getColorDepth) | Ottiene la profondità di colore per la firma digitale. |
| [getComments()](#getComments) | Specifica i commenti sulla firma digitale. |
| [getDecryptionPassword()](#getDecryptionPassword) | La password per decrittare il documento di origine. |
| [getHorizontalResolution()](#getHorizontalResolution) | Restituisce la risoluzione orizzontale per la firma digitale. |
| [getOfficeVersion()](#getOfficeVersion) | Restituisce la versione di Office per la firma digitale. |
| [getProviderId()](#getProviderId) | Specifica l'ID classe del provider della firma. |
| [getSignTime()](#getSignTime) | La data della firma. |
| [getSignatureLineId()](#getSignatureLineId) | Identificatore della riga firma. |
| [getSignatureLineImage()](#getSignatureLineImage) | L'immagine che verrà mostrata nella [SignatureLine](../../com.aspose.words/signatureline/) associata. |
| [getVerticalResolution()](#getVerticalResolution) | Restituisce la risoluzione verticale per la firma digitale. |
| [getWindowsVersion()](#getWindowsVersion) | Restituisce la versione di Windows per la firma digitale. |
| [getXmlDsigLevel()](#getXmlDsigLevel) | Specifica il livello di una firma digitale basata sullo standard XML-DSig. |
| [setApplicationVersion(String value)](#setApplicationVersion-java.lang.String) | Imposta la versione dell'applicazione per la firma digitale. |
| [setColorDepth(int value)](#setColorDepth-int) | Imposta la profondità di colore per la firma digitale. |
| [setComments(String value)](#setComments-java.lang.String) | Specifica i commenti sulla firma digitale. |
| [setDecryptionPassword(String value)](#setDecryptionPassword-java.lang.String) | La password per decrittare il documento di origine. |
| [setHorizontalResolution(int value)](#setHorizontalResolution-int) | Imposta la risoluzione orizzontale per la firma digitale. |
| [setOfficeVersion(String value)](#setOfficeVersion-java.lang.String) | Imposta la versione di Office per la firma digitale. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID) | Specifica l'ID classe del provider della firma. |
| [setSignTime(Date value)](#setSignTime-java.util.Date) | La data della firma. |
| [setSignatureLineId(UUID value)](#setSignatureLineId-java.util.UUID) | Identificatore della riga firma. |
| [setSignatureLineImage(byte[] value)](#setSignatureLineImage-byte) | L'immagine che verrà mostrata nella [SignatureLine](../../com.aspose.words/signatureline/) associata. |
| [setVerticalResolution(int value)](#setVerticalResolution-int) | Imposta la risoluzione verticale per la firma digitale. |
| [setWindowsVersion(String value)](#setWindowsVersion-java.lang.String) | Imposta la versione di Windows per la firma digitale. |
| [setXmlDsigLevel(int value)](#setXmlDsigLevel-int) | Specifica il livello di una firma digitale basata sullo standard XML-DSig. |
### getApplicationVersion() {#getApplicationVersion}
```
public String getApplicationVersion()
```


Restituisce la versione dell'applicazione per la firma digitale. Il valore predefinito è "12.0".

 **Examples:** 

Mostra come firmare un documento con opzioni di firma aggiuntive.

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
java.lang.String - La versione dell'applicazione per la firma digitale.
### getColorDepth() {#getColorDepth}
```
public int getColorDepth()
```


Restituisce la profondità di colore per la firma digitale. Il valore predefinito è 32.

 **Examples:** 

Mostra come firmare un documento con opzioni di firma aggiuntive.

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
int - La profondità di colore per la firma digitale.
### getComments() {#getComments}
```
public String getComments()
```


Specifica i commenti sulla firma digitale. Il valore predefinito è **empty string**.

 **Examples:** 

Mostra come firmare digitalmente i documenti.

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
java.lang.String - Il valore java.lang.String corrispondente.
### getDecryptionPassword() {#getDecryptionPassword}
```
public String getDecryptionPassword()
```


La password per decrittare il documento di origine. Il valore predefinito è **empty string**.

 **Remarks:** 

Se il documento OOXML è crittografato, è necessario fornire la password di decrittazione per decrittare il documento di origine prima che venga firmato. Questo non è richiesto per i documenti in formato binario DOC.

 **Examples:** 

Mostra come firmare un file di documento crittografato.

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
java.lang.String - Il valore java.lang.String corrispondente.
### getHorizontalResolution() {#getHorizontalResolution}
```
public int getHorizontalResolution()
```


Restituisce la risoluzione orizzontale per la firma digitale. Il valore predefinito è 1920.

 **Examples:** 

Mostra come firmare un documento con opzioni di firma aggiuntive.

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
int - La risoluzione orizzontale per la firma digitale.
### getOfficeVersion() {#getOfficeVersion}
```
public String getOfficeVersion()
```


Ottiene la versione di Office per la firma digitale. Il valore predefinito è "12.0".

 **Examples:** 

Mostra come firmare un documento con opzioni di firma aggiuntive.

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
java.lang.String - La versione di Office per la firma digitale.
### getProviderId() {#getProviderId}
```
public UUID getProviderId()
```


Specifica l'ID della classe del provider di firma. Il valore predefinito è **Empty (all zeroes) Guid**.

 **Remarks:** 

Il provider di servizi crittografici (CSP) è un modulo software indipendente che esegue effettivamente gli algoritmi di crittografia per l'autenticazione, la codifica e la cifratura. MS Office riserva il valore \{00000000-0000-0000-0000-000000000000\} per il suo provider di firma predefinito.

Il GUID del provider aggiuntivamente installato dovrebbe essere ottenuto dalla documentazione fornita con il provider.

Inoltre, tutti i provider crittografici installati sono elencati nel registro di Windows. Si può trovare nel seguente percorso: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. Esiste una chiave chiamata "CP Service UUID" che corrisponde a un GUID del provider di firma.

 **Examples:** 

Mostra come firmare un documento con un certificato personale e una riga di firma.

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
java.util.UUID - Il valore corrispondente di java.util.UUID.
### getSignTime() {#getSignTime}
```
public Date getSignTime()
```


La data della firma. Il valore predefinito è **current time**

 **Examples:** 

Mostra come firmare digitalmente i documenti.

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
java.util.Date - Il valore corrispondente di java.util.Date.
### getSignatureLineId() {#getSignatureLineId}
```
public UUID getSignatureLineId()
```


Identificatore della riga di firma. Il valore predefinito è **Empty (all zeroes) Guid**.

 **Remarks:** 

Quando impostato, associa [SignatureLine](../../com.aspose.words/signatureline/) con la corrispondente [DigitalSignature](../../com.aspose.words/digitalsignature/).

 **Examples:** 

Mostra come aggiungere una riga di firma a un documento e poi firmarlo usando un certificato digitale.

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
java.util.UUID - Il valore corrispondente di java.util.UUID.
### getSignatureLineImage() {#getSignatureLineImage}
```
public byte[] getSignatureLineImage()
```


L'immagine che verrà mostrata nella [SignatureLine](../../com.aspose.words/signatureline/) associata. Il valore predefinito è  null .

 **Examples:** 

Mostra come aggiungere una riga di firma a un documento e poi firmarlo usando un certificato digitale.

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
byte[] - Il valore byte[] corrispondente.
### getVerticalResolution() {#getVerticalResolution}
```
public int getVerticalResolution()
```


Ottiene la risoluzione verticale per la firma digitale. Il valore predefinito è 1200.

 **Examples:** 

Mostra come firmare un documento con opzioni di firma aggiuntive.

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
int - La risoluzione verticale per la firma digitale.
### getWindowsVersion() {#getWindowsVersion}
```
public String getWindowsVersion()
```


Ottiene la versione di Windows per la firma digitale. Il valore predefinito è "6.1".

 **Examples:** 

Mostra come firmare un documento con opzioni di firma aggiuntive.

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
java.lang.String - La versione di Windows per la firma digitale.
### getXmlDsigLevel() {#getXmlDsigLevel}
```
public int getXmlDsigLevel()
```


Specifica il livello di una firma digitale basata sullo standard XML-DSig. Il valore predefinito è [XmlDsigLevel.XML\_D\_SIG](../../com.aspose.words/xmldsiglevel/\#XML-D-SIG).

 **Remarks:** 

Diversi livelli di firme XAdES possono essere creati a partire da Office 2010.

 **Examples:** 

Mostra come firmare un documento basato sullo standard XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Returns:**
int - Il valore intero corrispondente. Il valore restituito è una delle costanti di [XmlDsigLevel](../../com.aspose.words/xmldsiglevel/).
### setApplicationVersion(String value) {#setApplicationVersion-java.lang.String}
```
public void setApplicationVersion(String value)
```


Imposta la versione dell'applicazione per la firma digitale. Il valore predefinito è "12.0".

 **Examples:** 

Mostra come firmare un documento con opzioni di firma aggiuntive.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | La versione dell'applicazione per la firma digitale. |

### setColorDepth(int value) {#setColorDepth-int}
```
public void setColorDepth(int value)
```


Imposta la profondità di colore per la firma digitale. Il valore predefinito è 32.

 **Examples:** 

Mostra come firmare un documento con opzioni di firma aggiuntive.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | La profondità di colore per la firma digitale. |

### setComments(String value) {#setComments-java.lang.String}
```
public void setComments(String value)
```


Specifica i commenti sulla firma digitale. Il valore predefinito è **empty string**.

 **Examples:** 

Mostra come firmare digitalmente i documenti.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setDecryptionPassword(String value) {#setDecryptionPassword-java.lang.String}
```
public void setDecryptionPassword(String value)
```


La password per decrittare il documento di origine. Il valore predefinito è **empty string**.

 **Remarks:** 

Se il documento OOXML è crittografato, è necessario fornire la password di decrittazione per decrittare il documento di origine prima che venga firmato. Questo non è richiesto per i documenti in formato binario DOC.

 **Examples:** 

Mostra come firmare un file di documento crittografato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setHorizontalResolution(int value) {#setHorizontalResolution-int}
```
public void setHorizontalResolution(int value)
```


Imposta la risoluzione orizzontale per la firma digitale. Il valore predefinito è 1920.

 **Examples:** 

Mostra come firmare un documento con opzioni di firma aggiuntive.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | La risoluzione orizzontale per la firma digitale. |

### setOfficeVersion(String value) {#setOfficeVersion-java.lang.String}
```
public void setOfficeVersion(String value)
```


Imposta la versione di Office per la firma digitale. Il valore predefinito è "12.0".

 **Examples:** 

Mostra come firmare un documento con opzioni di firma aggiuntive.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | La versione di Office per la firma digitale. |

### setProviderId(UUID value) {#setProviderId-java.util.UUID}
```
public void setProviderId(UUID value)
```


Specifica l'ID della classe del provider di firma. Il valore predefinito è **Empty (all zeroes) Guid**.

 **Remarks:** 

Il provider di servizi crittografici (CSP) è un modulo software indipendente che esegue effettivamente gli algoritmi di crittografia per l'autenticazione, la codifica e la cifratura. MS Office riserva il valore \{00000000-0000-0000-0000-000000000000\} per il suo provider di firma predefinito.

Il GUID del provider aggiuntivamente installato dovrebbe essere ottenuto dalla documentazione fornita con il provider.

Inoltre, tutti i provider crittografici installati sono elencati nel registro di Windows. Si può trovare nel seguente percorso: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. Esiste una chiave chiamata "CP Service UUID" che corrisponde a un GUID del provider di firma.

 **Examples:** 

Mostra come firmare un documento con un certificato personale e una riga di firma.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.util.UUID | Il valore corrispondente java.util.UUID. |

### setSignTime(Date value) {#setSignTime-java.util.Date}
```
public void setSignTime(Date value)
```


La data della firma. Il valore predefinito è **current time**

 **Examples:** 

Mostra come firmare digitalmente i documenti.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.util.Date | Il valore corrispondente java.util.Date. |

### setSignatureLineId(UUID value) {#setSignatureLineId-java.util.UUID}
```
public void setSignatureLineId(UUID value)
```


Identificatore della riga di firma. Il valore predefinito è **Empty (all zeroes) Guid**.

 **Remarks:** 

Quando impostato, associa [SignatureLine](../../com.aspose.words/signatureline/) con la corrispondente [DigitalSignature](../../com.aspose.words/digitalsignature/).

 **Examples:** 

Mostra come aggiungere una riga di firma a un documento e poi firmarlo usando un certificato digitale.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.util.UUID | Il valore corrispondente java.util.UUID. |

### setSignatureLineImage(byte[] value) {#setSignatureLineImage-byte}
```
public void setSignatureLineImage(byte[] value)
```


L'immagine che verrà mostrata nella [SignatureLine](../../com.aspose.words/signatureline/) associata. Il valore predefinito è  null .

 **Examples:** 

Mostra come aggiungere una riga di firma a un documento e poi firmarlo usando un certificato digitale.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | byte[] | Il valore byte[] corrispondente. |

### setVerticalResolution(int value) {#setVerticalResolution-int}
```
public void setVerticalResolution(int value)
```


Imposta la risoluzione verticale per la firma digitale. Il valore predefinito è 1200.

 **Examples:** 

Mostra come firmare un documento con opzioni di firma aggiuntive.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | La risoluzione verticale per la firma digitale. |

### setWindowsVersion(String value) {#setWindowsVersion-java.lang.String}
```
public void setWindowsVersion(String value)
```


Imposta la versione di Windows per la firma digitale. Il valore predefinito è "6.1".

 **Examples:** 

Mostra come firmare un documento con opzioni di firma aggiuntive.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | La versione di Windows per la firma digitale. |

### setXmlDsigLevel(int value) {#setXmlDsigLevel-int}
```
public void setXmlDsigLevel(int value)
```


Specifica il livello di una firma digitale basata sullo standard XML-DSig. Il valore predefinito è [XmlDsigLevel.XML\_D\_SIG](../../com.aspose.words/xmldsiglevel/\#XML-D-SIG).

 **Remarks:** 

Diversi livelli di firme XAdES possono essere creati a partire da Office 2010.

 **Examples:** 

Mostra come firmare un documento basato sullo standard XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore corrispondente  int  . Il valore deve essere uno dei costanti [XmlDsigLevel](../../com.aspose.words/xmldsiglevel/) constants. |

