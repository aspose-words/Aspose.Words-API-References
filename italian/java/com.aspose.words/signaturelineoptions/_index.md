---
title: "SignatureLineOptions"
linktitle: "SignatureLineOptions"
second_title: "Aspose.Words per Java"
description: "Consente di specificare le opzioni per la linea di firma inserita in Java."
type: docs
weight: 622
url: /it/java/com.aspose.words/signaturelineoptions/
---

**Inheritance:**
java.lang.Object
```
public class SignatureLineOptions
```

Consente di specificare le opzioni per la linea di firma inserita. Utilizzato in [DocumentBuilder](../../com.aspose.words/documentbuilder/).

Per saperne di più, visita l'articolo di documentazione [ Work with Digital Signatures ][Work with Digital Signatures].

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


[Work with Digital Signatures]: https://docs.aspose.com/words/java/working-with-digital-signatures/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getAllowComments()](#getAllowComments) | Restituisce un valore che indica che il firmatario può aggiungere commenti nella finestra di dialogo Firma. |
| [getDefaultInstructions()](#getDefaultInstructions) | Ottiene un valore che indica che le istruzioni predefinite sono visualizzate nella finestra di dialogo Sign. |
| [getEmail()](#getEmail) | Ottiene l'indirizzo e‑mail del firmatario suggerito. |
| [getInstructions()](#getInstructions) | Ottiene le istruzioni per il firmatario che vengono visualizzate durante la firma della riga di firma. |
| [getShowDate()](#getShowDate) | Ottiene un valore che indica che la data di firma è visualizzata nella riga di firma. |
| [getSigner()](#getSigner) | Ottiene il firmatario suggerito della riga di firma. |
| [getSignerTitle()](#getSignerTitle) | Ottiene il titolo del firmatario suggerito. |
| [setAllowComments(boolean value)](#setAllowComments-boolean) | Imposta un valore che indica che il firmatario può aggiungere commenti nella finestra di dialogo Sign. |
| [setDefaultInstructions(boolean value)](#setDefaultInstructions-boolean) | Imposta un valore che indica che le istruzioni predefinite sono visualizzate nella finestra di dialogo Sign. |
| [setEmail(String value)](#setEmail-java.lang.String) | Imposta l'indirizzo e‑mail del firmatario suggerito. |
| [setInstructions(String value)](#setInstructions-java.lang.String) | Imposta le istruzioni per il firmatario che vengono visualizzate durante la firma della riga di firma. |
| [setShowDate(boolean value)](#setShowDate-boolean) | Imposta un valore che indica che la data di firma è visualizzata nella riga di firma. |
| [setSigner(String value)](#setSigner-java.lang.String) | Imposta il firmatario suggerito della riga di firma. |
| [setSignerTitle(String value)](#setSignerTitle-java.lang.String) | Imposta il titolo del firmatario suggerito. |
### getAllowComments() {#getAllowComments}
```
public boolean getAllowComments()
```


Ottiene un valore che indica che il firmatario può aggiungere commenti nella finestra di dialogo Sign. Il valore predefinito per questa proprietà è false.

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
boolean - Un valore che indica che il firmatario può aggiungere commenti nella finestra di dialogo Sign.
### getDefaultInstructions() {#getDefaultInstructions}
```
public boolean getDefaultInstructions()
```


Ottiene un valore che indica che le istruzioni predefinite sono visualizzate nella finestra di dialogo Sign. Il valore predefinito per questa proprietà è true.

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
boolean - Un valore che indica che le istruzioni predefinite sono visualizzate nella finestra di dialogo Sign.
### getEmail() {#getEmail}
```
public String getEmail()
```


Ottiene l'indirizzo e‑mail del firmatario suggerito. Il valore predefinito per questa proprietà è **empty string**.

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
java.lang.String - Indirizzo e‑mail del firmatario suggerito.
### getInstructions() {#getInstructions}
```
public String getInstructions()
```


Ottiene le istruzioni per il firmatario che vengono visualizzate durante la firma della riga di firma. Il valore predefinito per questa proprietà è **empty string**.

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
java.lang.String - Istruzioni per il firmatario che vengono visualizzate durante la firma della riga di firma.
### getShowDate() {#getShowDate}
```
public boolean getShowDate()
```


Ottiene un valore che indica che la data di firma è visualizzata nella riga di firma. Il valore predefinito per questa proprietà è true.

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
boolean - Un valore che indica che la data di firma è visualizzata nella riga di firma.
### getSigner() {#getSigner}
```
public String getSigner()
```


Ottiene il firmatario suggerito della riga di firma. Il valore predefinito per questa proprietà è **empty string**.

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
java.lang.String - Firmatario suggerito della riga di firma.
### getSignerTitle() {#getSignerTitle}
```
public String getSignerTitle()
```


Ottiene il titolo suggerito del firmatario. Il valore predefinito per questa proprietà è **empty string**.

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
java.lang.String - Titolo suggerito del firmatario.
### setAllowComments(boolean value) {#setAllowComments-boolean}
```
public void setAllowComments(boolean value)
```


Imposta un valore che indica che il firmatario può aggiungere commenti nella finestra di dialogo Sign. Il valore predefinito per questa proprietà è false.

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
| valore | boolean | Un valore che indica che il firmatario può aggiungere commenti nella finestra di dialogo Sign. |

### setDefaultInstructions(boolean value) {#setDefaultInstructions-boolean}
```
public void setDefaultInstructions(boolean value)
```


Imposta un valore che indica che le istruzioni predefinite sono visualizzate nella finestra di dialogo Sign. Il valore predefinito per questa proprietà è true.

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
| valore | boolean | Un valore che indica che le istruzioni predefinite sono visualizzate nella finestra di dialogo Sign. |

### setEmail(String value) {#setEmail-java.lang.String}
```
public void setEmail(String value)
```


Imposta l'indirizzo e‑mail suggerito del firmatario. Il valore predefinito per questa proprietà è **empty string**.

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
| valore | java.lang.String | Indirizzo e‑mail suggerito del firmatario. |

### setInstructions(String value) {#setInstructions-java.lang.String}
```
public void setInstructions(String value)
```


Imposta le istruzioni per il firmatario che vengono visualizzate durante la firma della linea di firma. Il valore predefinito per questa proprietà è **empty string**.

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
| valore | java.lang.String | Istruzioni per il firmatario che vengono visualizzate durante la firma della linea di firma. |

### setShowDate(boolean value) {#setShowDate-boolean}
```
public void setShowDate(boolean value)
```


Imposta un valore che indica che la data di firma è visualizzata nella linea di firma. Il valore predefinito per questa proprietà è true.

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
| valore | boolean | Un valore che indica che la data di firma è visualizzata nella linea di firma. |

### setSigner(String value) {#setSigner-java.lang.String}
```
public void setSigner(String value)
```


Imposta il firmatario suggerito della linea di firma. Il valore predefinito per questa proprietà è **empty string**.

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
| valore | java.lang.String | Firmatario suggerito della linea di firma. |

### setSignerTitle(String value) {#setSignerTitle-java.lang.String}
```
public void setSignerTitle(String value)
```


Imposta il titolo suggerito del firmatario. Il valore predefinito per questa proprietà è **empty string**.

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
| valore | java.lang.String | Titolo suggerito del firmatario. |

