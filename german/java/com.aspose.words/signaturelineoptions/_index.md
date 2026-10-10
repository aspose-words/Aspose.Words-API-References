---
title: "SignatureLineOptions"
linktitle: "SignatureLineOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Festlegen von Optionen für die Einfügung einer Signaturzeile in Java."
type: docs
weight: 622
url: /de/java/com.aspose.words/signaturelineoptions/
---

**Inheritance:**
java.lang.Object
```
public class SignatureLineOptions
```

Ermöglicht das Festlegen von Optionen für die Einfügung einer Signaturzeile. Verwendet in [DocumentBuilder](../../com.aspose.words/documentbuilder/).

Weitere Informationen finden Sie im Dokumentationsartikel [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAllowComments()](#getAllowComments) | Gibt einen Wert zurück, der angibt, dass der Unterzeichner Kommentare im Signaturdialog hinzufügen kann. |
| [getDefaultInstructions()](#getDefaultInstructions) | Gibt einen Wert zurück, der angibt, dass Standardanweisungen im Signaturdialog angezeigt werden. |
| [getEmail()](#getEmail) | Gibt die vorgeschlagene E‑Mail‑Adresse des Unterzeichners zurück. |
| [getInstructions()](#getInstructions) | Gibt Anweisungen an den Unterzeichner zurück, die beim Signieren der Signaturzeile angezeigt werden. |
| [getShowDate()](#getShowDate) | Gibt einen Wert zurück, der angibt, dass das Signaturdatum in der Signaturzeile angezeigt wird. |
| [getSigner()](#getSigner) | Gibt den vorgeschlagenen Unterzeichner der Signaturzeile zurück. |
| [getSignerTitle()](#getSignerTitle) | Gibt den vorgeschlagenen Titel des Unterzeichners zurück. |
| [setAllowComments(boolean value)](#setAllowComments-boolean) | Setzt einen Wert, der angibt, dass der Unterzeichner Kommentare im Signaturdialog hinzufügen kann. |
| [setDefaultInstructions(boolean value)](#setDefaultInstructions-boolean) | Setzt einen Wert, der angibt, dass Standardanweisungen im Signaturdialog angezeigt werden. |
| [setEmail(String value)](#setEmail-java.lang.String) | Setzt die vorgeschlagene E‑Mail‑Adresse des Unterzeichners. |
| [setInstructions(String value)](#setInstructions-java.lang.String) | Setzt Anweisungen an den Unterzeichner, die beim Signieren der Signaturzeile angezeigt werden. |
| [setShowDate(boolean value)](#setShowDate-boolean) | Setzt einen Wert, der angibt, dass das Signaturdatum in der Signaturzeile angezeigt wird. |
| [setSigner(String value)](#setSigner-java.lang.String) | Setzt den vorgeschlagenen Unterzeichner der Signaturzeile. |
| [setSignerTitle(String value)](#setSignerTitle-java.lang.String) | Setzt den vorgeschlagenen Titel des Unterzeichners. |
### getAllowComments() {#getAllowComments}
```
public boolean getAllowComments()
```


Gibt einen Wert zurück, der angibt, dass der Unterzeichner Kommentare im Signaturdialog hinzufügen kann. Der Standardwert für diese Eigenschaft ist  false .

 **Examples:** 

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

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
boolean - Ein Wert, der angibt, dass der Unterzeichner Kommentare im Sign-Dialog hinzufügen kann.
### getDefaultInstructions() {#getDefaultInstructions}
```
public boolean getDefaultInstructions()
```


Liefert einen Wert, der angibt, dass Standardanweisungen im Sign-Dialog angezeigt werden. Standardwert für diese Eigenschaft ist true.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

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
boolean - Ein Wert, der angibt, dass Standardanweisungen im Sign-Dialog angezeigt werden.
### getEmail() {#getEmail}
```
public String getEmail()
```


Liefert die vorgeschlagene E‑Mail‑Adresse des Unterzeichners. Standardwert für diese Eigenschaft ist **empty string**.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

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
java.lang.String - Vorgeschlagene E‑Mail‑Adresse des Unterzeichners.
### getInstructions() {#getInstructions}
```
public String getInstructions()
```


Liefert Anweisungen an den Unterzeichner, die beim Signieren der Signaturzeile angezeigt werden. Standardwert für diese Eigenschaft ist **empty string**.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

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
java.lang.String - Anweisungen an den Unterzeichner, die beim Signieren der Signaturzeile angezeigt werden.
### getShowDate() {#getShowDate}
```
public boolean getShowDate()
```


Liefert einen Wert, der angibt, dass das Signaturdatum in der Signaturzeile angezeigt wird. Standardwert für diese Eigenschaft ist true.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

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
boolean - Ein Wert, der angibt, dass das Signaturdatum in der Signaturzeile angezeigt wird.
### getSigner() {#getSigner}
```
public String getSigner()
```


Liefert den vorgeschlagenen Unterzeichner der Signaturzeile. Standardwert für diese Eigenschaft ist **empty string**.

 **Examples:** 

Zeigt, wie man einer Datei eine Signaturzeile hinzufügt und sie anschließend mit einem digitalen Zertifikat signiert.

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
java.lang.String - Vorgeschlagener Unterzeichner der Signaturzeile.
### getSignerTitle() {#getSignerTitle}
```
public String getSignerTitle()
```


Liefert den vorgeschlagenen Titel des Unterzeichners. Standardwert für diese Eigenschaft ist **empty string**.

 **Examples:** 

Zeigt, wie man einer Datei eine Signaturzeile hinzufügt und sie anschließend mit einem digitalen Zertifikat signiert.

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
java.lang.String - Vorgeschlagener Titel des Unterzeichners.
### setAllowComments(boolean value) {#setAllowComments-boolean}
```
public void setAllowComments(boolean value)
```


Setzt einen Wert, der angibt, dass der Unterzeichner Kommentare im Sign-Dialog hinzufügen kann. Standardwert für diese Eigenschaft ist false.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der angibt, dass der Unterzeichner Kommentare im Sign-Dialog hinzufügen kann. |

### setDefaultInstructions(boolean value) {#setDefaultInstructions-boolean}
```
public void setDefaultInstructions(boolean value)
```


Setzt einen Wert, der angibt, dass Standardanweisungen im Sign-Dialog angezeigt werden. Standardwert für diese Eigenschaft ist true.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der angibt, dass Standardanweisungen im Sign-Dialog angezeigt werden. |

### setEmail(String value) {#setEmail-java.lang.String}
```
public void setEmail(String value)
```


Setzt die vorgeschlagene E‑Mail‑Adresse des Unterzeichners. Standardwert für diese Eigenschaft ist **empty string**.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Vorgeschlagene E‑Mail‑Adresse des Unterzeichners. |

### setInstructions(String value) {#setInstructions-java.lang.String}
```
public void setInstructions(String value)
```


Setzt Anweisungen an den Unterzeichner, die beim Signieren der Signaturzeile angezeigt werden. Standardwert für diese Eigenschaft ist **empty string**.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Anweisungen an den Unterzeichner, die beim Signieren der Signaturzeile angezeigt werden. |

### setShowDate(boolean value) {#setShowDate-boolean}
```
public void setShowDate(boolean value)
```


Setzt einen Wert, der angibt, dass das Signaturdatum in der Signaturzeile angezeigt wird. Standardwert für diese Eigenschaft ist true.

 **Examples:** 

Zeigt, wie man ein Dokument mit einem persönlichen Zertifikat und einer Signaturzeile signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der angibt, dass das Signaturdatum in der Signaturzeile angezeigt wird. |

### setSigner(String value) {#setSigner-java.lang.String}
```
public void setSigner(String value)
```


Setzt den vorgeschlagenen Unterzeichner der Signaturzeile. Standardwert für diese Eigenschaft ist **empty string**.

 **Examples:** 

Zeigt, wie man einer Datei eine Signaturzeile hinzufügt und sie anschließend mit einem digitalen Zertifikat signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Vorgeschlagener Unterzeichner der Signaturzeile. |

### setSignerTitle(String value) {#setSignerTitle-java.lang.String}
```
public void setSignerTitle(String value)
```


Legt den vorgeschlagenen Titel des Unterzeichners fest. Der Standardwert für diese Eigenschaft ist **leerer String**.

 **Examples:** 

Zeigt, wie man einer Datei eine Signaturzeile hinzufügt und sie anschließend mit einem digitalen Zertifikat signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Vorgeschlagener Titel des Unterzeichners. |

