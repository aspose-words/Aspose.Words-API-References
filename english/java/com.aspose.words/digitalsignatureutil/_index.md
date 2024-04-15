---
title: DigitalSignatureUtil
linktitle: DigitalSignatureUtil
second_title: Aspose.Words for Java
description: Provides methods for signing document in Java.
type: docs
weight: 135
url: /java/com.aspose.words/digitalsignatureutil/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignatureUtil
```

Provides methods for signing document.

To learn more, visit the [ Work with Digital Signatures ][Work with Digital Signatures] documentation article.

 **Remarks:** 

Since digital signature works with file content rather than Document Object Model these methods are put into a separate class.

Supported formats are: [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT).

 **Examples:** 

Shows how to load signatures from a digitally signed document.

```

 // There are two ways of loading a signed document's collection of digital signatures using the DigitalSignatureUtil class.
 // 1 -  Load from a document from a local file system filename:
 DigitalSignatureCollection digitalSignatures =
         DigitalSignatureUtil.loadSignatures(getMyDir() + "Digitally signed.docx");

 // If this collection is nonempty, then we can verify that the document is digitally signed.
 Assert.assertEquals(1, digitalSignatures.getCount());

 // 2 -  Load from a document from a FileStream:
 InputStream stream = new FileInputStream(getMyDir() + "Digitally signed.docx");
 try {
     digitalSignatures = DigitalSignatureUtil.loadSignatures(stream);
     Assert.assertEquals(1, digitalSignatures.getCount());
 } finally {
     if (stream != null) stream.close();
 }
 
```

Shows how to remove digital signatures from a digitally signed document.

```

 // There are two ways of using the DigitalSignatureUtil class to remove digital signatures
 // from a signed document by saving an unsigned copy of it somewhere else in the local file system.
 // 1 - Determine the locations of both the signed document and the unsigned copy by filename strings:
 DigitalSignatureUtil.removeAllSignatures(getMyDir() + "Digitally signed.docx",
         getArtifactsDir() + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

 // 2 - Determine the locations of both the signed document and the unsigned copy by file streams:
 InputStream streamIn = new FileInputStream(getMyDir() + "Digitally signed.docx");
 try {
     OutputStream streamOut = new FileOutputStream(getArtifactsDir() + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx");
     try {
         DigitalSignatureUtil.removeAllSignatures(streamIn, streamOut);
     } finally {
         if (streamOut != null) streamOut.close();
     }
 } finally {
     if (streamIn != null) streamIn.close();
 }

 // Verify that both our output documents have no digital signatures.
 Assert.assertEquals(DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").getCount(), 0);
 Assert.assertEquals(DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").getCount(), 0);
 
```


[Work with Digital Signatures]: https://docs.aspose.com/words/java/working-with-digital-signatures/
## Methods

| Method | Description |
| --- | --- |
| [loadSignatures(InputStream stream)](#loadSignatures-java.io.InputStream) |  |
| [loadSignatures(String fileName)](#loadSignatures-java.lang.String) | Loads digital signatures from document. |
| [removeAllSignatures(InputStream srcStream, OutputStream dstStream)](#removeAllSignatures-java.io.InputStream-java.io.OutputStream) |  |
| [removeAllSignatures(String srcFileName, String dstFileName)](#removeAllSignatures-java.lang.String-java.lang.String) | Removes all digital signatures from source file and writes unsigned file to destination file. |
| [sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder)](#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder) |  |
| [sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder, SignOptions signOptions)](#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions) |  |
| [sign(String srcFileName, String dstFileName, CertificateHolder certHolder)](#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder) | Signs source document using given [CertificateHolder](../../com.aspose.words/certificateholder/) with digital signature and writes signed document to destination file. |
| [sign(String srcFileName, String dstFileName, CertificateHolder certHolder, SignOptions signOptions)](#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions) | Signs source document using given [CertificateHolder](../../com.aspose.words/certificateholder/) and [SignOptions](../../com.aspose.words/signoptions/) with digital signature and writes signed document to destination file. |
### loadSignatures(InputStream stream) {#loadSignatures-java.io.InputStream}
```
public static DigitalSignatureCollection loadSignatures(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection/)
### loadSignatures(String fileName) {#loadSignatures-java.lang.String}
```
public static DigitalSignatureCollection loadSignatures(String fileName)
```


Loads digital signatures from document.

 **Examples:** 

Shows how to load signatures from a digitally signed document.

```

 // There are two ways of loading a signed document's collection of digital signatures using the DigitalSignatureUtil class.
 // 1 -  Load from a document from a local file system filename:
 DigitalSignatureCollection digitalSignatures =
         DigitalSignatureUtil.loadSignatures(getMyDir() + "Digitally signed.docx");

 // If this collection is nonempty, then we can verify that the document is digitally signed.
 Assert.assertEquals(1, digitalSignatures.getCount());

 // 2 -  Load from a document from a FileStream:
 InputStream stream = new FileInputStream(getMyDir() + "Digitally signed.docx");
 try {
     digitalSignatures = DigitalSignatureUtil.loadSignatures(stream);
     Assert.assertEquals(1, digitalSignatures.getCount());
 } finally {
     if (stream != null) stream.close();
 }
 
```

Shows how to remove digital signatures from a digitally signed document.

```

 // There are two ways of using the DigitalSignatureUtil class to remove digital signatures
 // from a signed document by saving an unsigned copy of it somewhere else in the local file system.
 // 1 - Determine the locations of both the signed document and the unsigned copy by filename strings:
 DigitalSignatureUtil.removeAllSignatures(getMyDir() + "Digitally signed.docx",
         getArtifactsDir() + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

 // 2 - Determine the locations of both the signed document and the unsigned copy by file streams:
 InputStream streamIn = new FileInputStream(getMyDir() + "Digitally signed.docx");
 try {
     OutputStream streamOut = new FileOutputStream(getArtifactsDir() + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx");
     try {
         DigitalSignatureUtil.removeAllSignatures(streamIn, streamOut);
     } finally {
         if (streamOut != null) streamOut.close();
     }
 } finally {
     if (streamIn != null) streamIn.close();
 }

 // Verify that both our output documents have no digital signatures.
 Assert.assertEquals(DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").getCount(), 0);
 Assert.assertEquals(DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").getCount(), 0);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Path to the document. |

**Returns:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection/) - Collection of digital signatures. Returns empty collection if file is not signed.
### removeAllSignatures(InputStream srcStream, OutputStream dstStream) {#removeAllSignatures-java.io.InputStream-java.io.OutputStream}
```
public static void removeAllSignatures(InputStream srcStream, OutputStream dstStream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | java.io.InputStream |  |
| dstStream | java.io.OutputStream |  |

### removeAllSignatures(String srcFileName, String dstFileName) {#removeAllSignatures-java.lang.String-java.lang.String}
```
public static void removeAllSignatures(String srcFileName, String dstFileName)
```


Removes all digital signatures from source file and writes unsigned file to destination file.

The following formats are compatible for digital signature removal: [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT).

 **Examples:** 

Shows how to remove digital signatures from a digitally signed document.

```

 // There are two ways of using the DigitalSignatureUtil class to remove digital signatures
 // from a signed document by saving an unsigned copy of it somewhere else in the local file system.
 // 1 - Determine the locations of both the signed document and the unsigned copy by filename strings:
 DigitalSignatureUtil.removeAllSignatures(getMyDir() + "Digitally signed.docx",
         getArtifactsDir() + "DigitalSignatureUtil.LoadAndRemove.FromString.docx");

 // 2 - Determine the locations of both the signed document and the unsigned copy by file streams:
 InputStream streamIn = new FileInputStream(getMyDir() + "Digitally signed.docx");
 try {
     OutputStream streamOut = new FileOutputStream(getArtifactsDir() + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx");
     try {
         DigitalSignatureUtil.removeAllSignatures(streamIn, streamOut);
     } finally {
         if (streamOut != null) streamOut.close();
     }
 } finally {
     if (streamIn != null) streamIn.close();
 }

 // Verify that both our output documents have no digital signatures.
 Assert.assertEquals(DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "DigitalSignatureUtil.LoadAndRemove.FromString.docx").getCount(), 0);
 Assert.assertEquals(DigitalSignatureUtil.loadSignatures(getArtifactsDir() + "DigitalSignatureUtil.LoadAndRemove.FromStream.docx").getCount(), 0);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | java.lang.String |  |
| dstFileName | java.lang.String |  |

### sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder) {#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder}
```
public static void sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | java.io.InputStream |  |
| dstStream | java.io.OutputStream |  |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) |  |

### sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder, SignOptions signOptions) {#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions}
```
public static void sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder, SignOptions signOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | java.io.InputStream |  |
| dstStream | java.io.OutputStream |  |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) |  |
| signOptions | [SignOptions](../../com.aspose.words/signoptions/) |  |

### sign(String srcFileName, String dstFileName, CertificateHolder certHolder) {#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder}
```
public static void sign(String srcFileName, String dstFileName, CertificateHolder certHolder)
```


Signs source document using given [CertificateHolder](../../com.aspose.words/certificateholder/) with digital signature and writes signed document to destination file.

Supported formats are: [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT).

 **Examples:** 

Shows how to sign documents with X.509 certificates.

```

 // Verify that a document is not signed.
 Assert.assertFalse(FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx").hasDigitalSignature());

 // Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);

 SignOptions signOptions = new SignOptions();
 signOptions.setSignTime(new Date());

 // There are two ways of saving a signed copy of a document to the local file system:
 // 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "Document.DigitalSignature.docx",
         certificateHolder, signOptions);

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // 2 - Take a document from a stream, and save a signed copy to another stream.
 InputStream inDoc = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream outDoc = new FileOutputStream(getArtifactsDir() + "Document.DigitalSignature.docx");
     try {
         DigitalSignatureUtil.sign(inDoc, outDoc, certificateHolder);
     } finally {
         if (outDoc != null) outDoc.close();
     }
 } finally {
     if (inDoc != null) inDoc.close();
 }

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // Please verify that all of the document's digital signatures are valid and check their details.
 Document signedDoc = new Document(getArtifactsDir() + "Document.DigitalSignature.docx");
 DigitalSignatureCollection digitalSignatureCollection = signedDoc.getDigitalSignatures();

 Assert.assertTrue(digitalSignatureCollection.isValid());
 Assert.assertEquals(1, digitalSignatureCollection.getCount());
 Assert.assertEquals(DigitalSignatureType.XML_DSIG, digitalSignatureCollection.get(0).getSignatureType());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getIssuerName());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getSubjectName());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | java.lang.String | The file name of the document to sign. |
| dstFileName | java.lang.String | The file name of the signed document output. |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) | [CertificateHolder](../../com.aspose.words/certificateholder/) object with certificate that used to sign file. |

### sign(String srcFileName, String dstFileName, CertificateHolder certHolder, SignOptions signOptions) {#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions}
```
public static void sign(String srcFileName, String dstFileName, CertificateHolder certHolder, SignOptions signOptions)
```


Signs source document using given [CertificateHolder](../../com.aspose.words/certificateholder/) and [SignOptions](../../com.aspose.words/signoptions/) with digital signature and writes signed document to destination file.

Supported formats are: [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT).

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
| srcFileName | java.lang.String | The file name of the document to sign. |
| dstFileName | java.lang.String | The file name of the signed document output. |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) | [CertificateHolder](../../com.aspose.words/certificateholder/) object with certificate that used to sign file. |
| signOptions | [SignOptions](../../com.aspose.words/signoptions/) | [SignOptions](../../com.aspose.words/signoptions/) object with various signing options. |

