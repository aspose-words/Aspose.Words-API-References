---
title: SignatureLine
linktitle: SignatureLine
second_title: Aspose.Words for Java
description: Provides access to signature line properties in Java.
type: docs
weight: 582
url: /java/com.aspose.words/signatureline/
---

**Inheritance:**
java.lang.Object
```
public class SignatureLine
```

Provides access to signature line properties.

To learn more, visit the [ Work with Digital Signatures ][Work with Digital Signatures] documentation article.

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
## Methods

| Method | Description |
| --- | --- |
| [getAllowComments()](#getAllowComments) | Gets a value indicating that the signer can add comments in the Sign dialog. |
| [getDefaultInstructions()](#getDefaultInstructions) | Gets a value indicating that default instructions is shown in the Sign dialog. |
| [getEmail()](#getEmail) | Gets suggested signer's e-mail address. |
| [getId()](#getId) | Gets identifier for this signature line. |
| [getInstructions()](#getInstructions) | Gets instructions to the signer that are displayed on signing the signature line. |
| [getProviderId()](#getProviderId) | Gets signature provider identifier for this signature line. |
| [getShowDate()](#getShowDate) | Gets a value indicating that sign date is shown in the signature line. |
| [getSigner()](#getSigner) | Gets suggested signer of the signature line. |
| [getSignerTitle()](#getSignerTitle) | Gets suggested signer's title (for example, Manager). |
| [isSigned()](#isSigned) | Indicates that signature line is signed by digital signature. |
| [isValid()](#isValid) | Indicates that signature line is signed by digital signature and this digital signature is valid. |
| [setAllowComments(boolean value)](#setAllowComments-boolean) | Sets a value indicating that the signer can add comments in the Sign dialog. |
| [setDefaultInstructions(boolean value)](#setDefaultInstructions-boolean) | Sets a value indicating that default instructions is shown in the Sign dialog. |
| [setEmail(String value)](#setEmail-java.lang.String) | Sets suggested signer's e-mail address. |
| [setId(UUID value)](#setId-java.util.UUID) | Sets identifier for this signature line. |
| [setInstructions(String value)](#setInstructions-java.lang.String) | Sets instructions to the signer that are displayed on signing the signature line. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID) | Sets signature provider identifier for this signature line. |
| [setShowDate(boolean value)](#setShowDate-boolean) | Sets a value indicating that sign date is shown in the signature line. |
| [setSigner(String value)](#setSigner-java.lang.String) | Sets suggested signer of the signature line. |
| [setSignerTitle(String value)](#setSignerTitle-java.lang.String) | Sets suggested signer's title (for example, Manager). |
### getAllowComments() {#getAllowComments}
```
public boolean getAllowComments()
```


Gets a value indicating that the signer can add comments in the Sign dialog. Default value for this property is  false .

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
boolean - A value indicating that the signer can add comments in the Sign dialog.
### getDefaultInstructions() {#getDefaultInstructions}
```
public boolean getDefaultInstructions()
```


Gets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is  true .

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
boolean - A value indicating that default instructions is shown in the Sign dialog.
### getEmail() {#getEmail}
```
public String getEmail()
```


Gets suggested signer's e-mail address. Default value for this property is **empty string**.

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
java.lang.String - Suggested signer's e-mail address.
### getId() {#getId}
```
public UUID getId()
```


Gets identifier for this signature line.

This identifier can be associated with a digital signature, when signing document using [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil/). This value must be unique and by default it is randomly generated new Guid.

 **Examples:** 

Shows how to add a signature line to a document, and then sign it using a digital certificate.

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
java.util.UUID - Identifier for this signature line.
### getInstructions() {#getInstructions}
```
public String getInstructions()
```


Gets instructions to the signer that are displayed on signing the signature line. This property is ignored if [getDefaultInstructions()](../../com.aspose.words/signatureline/\#getDefaultInstructions) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline/\#setDefaultInstructions-boolean) is set. Default value for this property is **empty string**.

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
java.lang.String - Instructions to the signer that are displayed on signing the signature line.
### getProviderId() {#getProviderId}
```
public UUID getProviderId()
```


Gets signature provider identifier for this signature line. Default value is "\{00000000-0000-0000-0000-000000000000\}".

 **Remarks:** 

The cryptographic service provider (CSP) is an independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption. MS Office reserves the value of \{00000000-0000-0000-0000-000000000000\} for its default signature provider.

The GUID of the additionally installed provider should be obtained from the documentation shipped with the provider.

In addition, all the installed cryptographic providers are enumerated in windows registry. It can be found in the following path: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. There is a key name "CP Service UUID" which corresponds to a GUID of signature provider.

 **Examples:** 

Shows how to sign a document with a personal certificate and a signature line.

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
java.util.UUID - Signature provider identifier for this signature line.
### getShowDate() {#getShowDate}
```
public boolean getShowDate()
```


Gets a value indicating that sign date is shown in the signature line. Default value for this property is  true .

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
boolean - A value indicating that sign date is shown in the signature line.
### getSigner() {#getSigner}
```
public String getSigner()
```


Gets suggested signer of the signature line. Default value for this property is **empty string**.

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
java.lang.String - Suggested signer of the signature line.
### getSignerTitle() {#getSignerTitle}
```
public String getSignerTitle()
```


Gets suggested signer's title (for example, Manager). Default value for this property is **empty string**.

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
java.lang.String - Suggested signer's title (for example, Manager).
### isSigned() {#isSigned}
```
public boolean isSigned()
```


Indicates that signature line is signed by digital signature.

 **Examples:** 

Shows how to sign a document with a personal certificate and a signature line.

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
boolean - The corresponding  boolean  value.
### isValid() {#isValid}
```
public boolean isValid()
```


Indicates that signature line is signed by digital signature and this digital signature is valid.

 **Examples:** 

Shows how to sign a document with a personal certificate and a signature line.

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
boolean - The corresponding  boolean  value.
### setAllowComments(boolean value) {#setAllowComments-boolean}
```
public void setAllowComments(boolean value)
```


Sets a value indicating that the signer can add comments in the Sign dialog. Default value for this property is  false .

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating that the signer can add comments in the Sign dialog. |

### setDefaultInstructions(boolean value) {#setDefaultInstructions-boolean}
```
public void setDefaultInstructions(boolean value)
```


Sets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is  true .

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating that default instructions is shown in the Sign dialog. |

### setEmail(String value) {#setEmail-java.lang.String}
```
public void setEmail(String value)
```


Sets suggested signer's e-mail address. Default value for this property is **empty string**.

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Suggested signer's e-mail address. |

### setId(UUID value) {#setId-java.util.UUID}
```
public void setId(UUID value)
```


Sets identifier for this signature line.

This identifier can be associated with a digital signature, when signing document using [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil/). This value must be unique and by default it is randomly generated new Guid.

 **Examples:** 

Shows how to add a signature line to a document, and then sign it using a digital certificate.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.UUID | Identifier for this signature line. |

### setInstructions(String value) {#setInstructions-java.lang.String}
```
public void setInstructions(String value)
```


Sets instructions to the signer that are displayed on signing the signature line. This property is ignored if [getDefaultInstructions()](../../com.aspose.words/signatureline/\#getDefaultInstructions) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline/\#setDefaultInstructions-boolean) is set. Default value for this property is **empty string**.

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Instructions to the signer that are displayed on signing the signature line. |

### setProviderId(UUID value) {#setProviderId-java.util.UUID}
```
public void setProviderId(UUID value)
```


Sets signature provider identifier for this signature line. Default value is "\{00000000-0000-0000-0000-000000000000\}".

 **Remarks:** 

The cryptographic service provider (CSP) is an independent software module that actually performs cryptography algorithms for authentication, encoding, and encryption. MS Office reserves the value of \{00000000-0000-0000-0000-000000000000\} for its default signature provider.

The GUID of the additionally installed provider should be obtained from the documentation shipped with the provider.

In addition, all the installed cryptographic providers are enumerated in windows registry. It can be found in the following path: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. There is a key name "CP Service UUID" which corresponds to a GUID of signature provider.

 **Examples:** 

Shows how to sign a document with a personal certificate and a signature line.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.UUID | Signature provider identifier for this signature line. |

### setShowDate(boolean value) {#setShowDate-boolean}
```
public void setShowDate(boolean value)
```


Sets a value indicating that sign date is shown in the signature line. Default value for this property is  true .

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating that sign date is shown in the signature line. |

### setSigner(String value) {#setSigner-java.lang.String}
```
public void setSigner(String value)
```


Sets suggested signer of the signature line. Default value for this property is **empty string**.

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Suggested signer of the signature line. |

### setSignerTitle(String value) {#setSignerTitle-java.lang.String}
```
public void setSignerTitle(String value)
```


Sets suggested signer's title (for example, Manager). Default value for this property is **empty string**.

 **Examples:** 

Shows how to create a line for a signature and insert it into a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Suggested signer's title (for example, Manager). |

