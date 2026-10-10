---
title: "SignOptions"
linktitle: "SignOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد خيارات توقيع المستند في جافا."
type: docs
weight: 620
url: /ar/java/com.aspose.words/signoptions/
---

**Inheritance:**
java.lang.Object
```
public class SignOptions
```

يسمح بتحديد خيارات توقيع المستند.

لمزيد من المعلومات، زر مقالة الوثائق [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

يعرض كيفية توقيع المستندات رقميًا.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getApplicationVersion()](#getApplicationVersion) | يحصل على إصدار التطبيق للتوقيع الرقمي. |
| [getColorDepth()](#getColorDepth) | يحصل على عمق اللون للتوقيع الرقمي. |
| [getComments()](#getComments) | يحدد التعليقات على التوقيع الرقمي. |
| [getDecryptionPassword()](#getDecryptionPassword) | كلمة المرور لفك تشفير المستند المصدر. |
| [getHorizontalResolution()](#getHorizontalResolution) | يحصل على الدقة الأفقية للتوقيع الرقمي. |
| [getOfficeVersion()](#getOfficeVersion) | يحصل على إصدار Office للتوقيع الرقمي. |
| [getProviderId()](#getProviderId) | يحدد معرف الفئة لمزود التوقيع. |
| [getSignTime()](#getSignTime) | تاريخ التوقيع. |
| [getSignatureLineId()](#getSignatureLineId) | معرف سطر التوقيع. |
| [getSignatureLineImage()](#getSignatureLineImage) | الصورة التي ستظهر في [SignatureLine](../../com.aspose.words/signatureline/) المرتبطة. |
| [getVerticalResolution()](#getVerticalResolution) | يحصل على الدقة العمودية للتوقيع الرقمي. |
| [getWindowsVersion()](#getWindowsVersion) | يحصل على إصدار Windows للتوقيع الرقمي. |
| [getXmlDsigLevel()](#getXmlDsigLevel) | يحدد مستوى التوقيع الرقمي بناءً على معيار XML-DSig. |
| [setApplicationVersion(String value)](#setApplicationVersion-java.lang.String) | يضبط إصدار التطبيق للتوقيع الرقمي. |
| [setColorDepth(int value)](#setColorDepth-int) | يضبط عمق اللون للتوقيع الرقمي. |
| [setComments(String value)](#setComments-java.lang.String) | يحدد التعليقات على التوقيع الرقمي. |
| [setDecryptionPassword(String value)](#setDecryptionPassword-java.lang.String) | كلمة المرور لفك تشفير المستند المصدر. |
| [setHorizontalResolution(int value)](#setHorizontalResolution-int) | يضبط الدقة الأفقية للتوقيع الرقمي. |
| [setOfficeVersion(String value)](#setOfficeVersion-java.lang.String) | يضبط إصدار Office للتوقيع الرقمي. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID) | يحدد معرف الفئة لمزود التوقيع. |
| [setSignTime(Date value)](#setSignTime-java.util.Date) | تاريخ التوقيع. |
| [setSignatureLineId(UUID value)](#setSignatureLineId-java.util.UUID) | معرف سطر التوقيع. |
| [setSignatureLineImage(byte[] value)](#setSignatureLineImage-byte) | الصورة التي ستظهر في [SignatureLine](../../com.aspose.words/signatureline/) المرتبطة. |
| [setVerticalResolution(int value)](#setVerticalResolution-int) | يضبط الدقة العمودية للتوقيع الرقمي. |
| [setWindowsVersion(String value)](#setWindowsVersion-java.lang.String) | يضبط إصدار Windows للتوقيع الرقمي. |
| [setXmlDsigLevel(int value)](#setXmlDsigLevel-int) | يحدد مستوى التوقيع الرقمي بناءً على معيار XML-DSig. |
### getApplicationVersion() {#getApplicationVersion}
```
public String getApplicationVersion()
```


يحصل على إصدار التطبيق للتوقيع الرقمي. القيمة الافتراضية هي "12.0".

 **Examples:** 

يعرض كيفية توقيع مستند مع خيارات توقيع إضافية.

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
java.lang.String - إصدار التطبيق للتوقيع الرقمي.
### getColorDepth() {#getColorDepth}
```
public int getColorDepth()
```


يحصل على عمق اللون للتوقيع الرقمي. القيمة الافتراضية هي 32.

 **Examples:** 

يعرض كيفية توقيع مستند مع خيارات توقيع إضافية.

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
int - عمق اللون للتوقيع الرقمي.
### getComments() {#getComments}
```
public String getComments()
```


يحدد التعليقات على التوقيع الرقمي. القيمة الافتراضية هي **empty string**.

 **Examples:** 

يعرض كيفية توقيع المستندات رقميًا.

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
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getDecryptionPassword() {#getDecryptionPassword}
```
public String getDecryptionPassword()
```


كلمة المرور لفك تشفير المستند المصدر. القيمة الافتراضية هي **empty string**.

 **Remarks:** 

إذا كان مستند OOXML مشفرًا، يجب عليك توفير كلمة مرور فك التشفير لفك تشفير المستند المصدر قبل توقيعه. هذا غير مطلوب للمستندات بصيغة DOC الثنائية.

 **Examples:** 

يوضح كيفية توقيع ملف مستند مشفر.

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
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getHorizontalResolution() {#getHorizontalResolution}
```
public int getHorizontalResolution()
```


يحصل على الدقة الأفقية للتوقيع الرقمي. القيمة الافتراضية هي 1920.

 **Examples:** 

يعرض كيفية توقيع مستند مع خيارات توقيع إضافية.

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
int - الدقة الأفقية للتوقيع الرقمي.
### getOfficeVersion() {#getOfficeVersion}
```
public String getOfficeVersion()
```


يحصل على إصدار Office للتوقيع الرقمي. القيمة الافتراضية هي "12.0".

 **Examples:** 

يعرض كيفية توقيع مستند مع خيارات توقيع إضافية.

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
java.lang.String - إصدار Office للتوقيع الرقمي.
### getProviderId() {#getProviderId}
```
public UUID getProviderId()
```


يحدد معرف الفئة لمزود التوقيع. القيمة الافتراضية هي **Empty (all zeroes) Guid**.

 **Remarks:** 

مزود خدمة التشفير (CSP) هو وحدة برمجية مستقلة تقوم فعليًا بتنفيذ خوارزميات التشفير للمصادقة والترميز والتشفير. يحتفظ MS Office بالقيمة \\{00000000-0000-0000-0000-000000000000\\} لمزود التوقيع الافتراضي الخاص به.

يجب الحصول على GUID للمزود المثبت إضافيًا من الوثائق المرفقة مع المزود.

بالإضافة إلى ذلك، يتم تعداد جميع مزودي التشفير المثبتين في سجل Windows. يمكن العثور عليه في المسار التالي: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. هناك اسم مفتاح "CP Service UUID" الذي يتطابق مع GUID لمزود التوقيع.

 **Examples:** 

يعرض كيفية توقيع مستند بشهادة شخصية وسطر توقيع.

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
java.util.UUID - القيمة المقابلة لـ java.util.UUID.
### getSignTime() {#getSignTime}
```
public Date getSignTime()
```


تاريخ التوقيع. القيمة الافتراضية هي **current time**

 **Examples:** 

يعرض كيفية توقيع المستندات رقميًا.

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
java.util.Date - القيمة المقابلة لـ java.util.Date.
### getSignatureLineId() {#getSignatureLineId}
```
public UUID getSignatureLineId()
```


معرف سطر التوقيع. القيمة الافتراضية هي **Empty (all zeroes) Guid**.

 **Remarks:** 

عند الضبط، يربط [SignatureLine](../../com.aspose.words/signatureline/) بـ [DigitalSignature](../../com.aspose.words/digitalsignature/) المقابل.

 **Examples:** 

يعرض كيفية إضافة سطر توقيع إلى مستند، ثم توقيعه باستخدام شهادة رقمية.

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
java.util.UUID - القيمة المقابلة لـ java.util.UUID.
### getSignatureLineImage() {#getSignatureLineImage}
```
public byte[] getSignatureLineImage()
```


الصورة التي سيتم عرضها في [SignatureLine](../../com.aspose.words/signatureline/) المرتبط. القيمة الافتراضية هي null.

 **Examples:** 

يعرض كيفية إضافة سطر توقيع إلى مستند، ثم توقيعه باستخدام شهادة رقمية.

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
byte[] - القيمة المقابلة من نوع byte[] .
### getVerticalResolution() {#getVerticalResolution}
```
public int getVerticalResolution()
```


يحصل على الدقة العمودية للتوقيع الرقمي. القيمة الافتراضية هي 1200.

 **Examples:** 

يعرض كيفية توقيع مستند مع خيارات توقيع إضافية.

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
int - الدقة العمودية للتوقيع الرقمي.
### getWindowsVersion() {#getWindowsVersion}
```
public String getWindowsVersion()
```


يحصل على إصدار Windows للتوقيع الرقمي. القيمة الافتراضية هي "6.1".

 **Examples:** 

يعرض كيفية توقيع مستند مع خيارات توقيع إضافية.

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
java.lang.String - إصدار Windows للتوقيع الرقمي.
### getXmlDsigLevel() {#getXmlDsigLevel}
```
public int getXmlDsigLevel()
```


يحدد مستوى التوقيع الرقمي بناءً على معيار XML-DSig. القيمة الافتراضية هي [XmlDsigLevel.XML\_D\_SIG](../../com.aspose.words/xmldsiglevel/\#XML-D-SIG).

 **Remarks:** 

يمكن إنشاء مستويات مختلفة من توقيعات XAdES بدءًا من Office 2010.

 **Examples:** 

يعرض كيفية توقيع مستند بناءً على معيار XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Returns:**
int - القيمة المقابلة من نوع int. القيمة المرجعة هي واحدة من ثوابت [XmlDsigLevel](../../com.aspose.words/xmldsiglevel/).
### setApplicationVersion(String value) {#setApplicationVersion-java.lang.String}
```
public void setApplicationVersion(String value)
```


يضبط إصدار التطبيق للتوقيع الرقمي. القيمة الافتراضية هي "12.0".

 **Examples:** 

يعرض كيفية توقيع مستند مع خيارات توقيع إضافية.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | إصدار التطبيق للتوقيع الرقمي. |

### setColorDepth(int value) {#setColorDepth-int}
```
public void setColorDepth(int value)
```


يضبط عمق اللون للتوقيع الرقمي. القيمة الافتراضية هي 32.

 **Examples:** 

يعرض كيفية توقيع مستند مع خيارات توقيع إضافية.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | عمق اللون للتوقيع الرقمي. |

### setComments(String value) {#setComments-java.lang.String}
```
public void setComments(String value)
```


يحدد التعليقات على التوقيع الرقمي. القيمة الافتراضية هي **empty string**.

 **Examples:** 

يعرض كيفية توقيع المستندات رقميًا.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setDecryptionPassword(String value) {#setDecryptionPassword-java.lang.String}
```
public void setDecryptionPassword(String value)
```


كلمة المرور لفك تشفير المستند المصدر. القيمة الافتراضية هي **empty string**.

 **Remarks:** 

إذا كان مستند OOXML مشفرًا، يجب عليك توفير كلمة مرور فك التشفير لفك تشفير المستند المصدر قبل توقيعه. هذا غير مطلوب للمستندات بصيغة DOC الثنائية.

 **Examples:** 

يوضح كيفية توقيع ملف مستند مشفر.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setHorizontalResolution(int value) {#setHorizontalResolution-int}
```
public void setHorizontalResolution(int value)
```


يضبط الدقة الأفقية للتوقيع الرقمي. القيمة الافتراضية هي 1920.

 **Examples:** 

يعرض كيفية توقيع مستند مع خيارات توقيع إضافية.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | الدقة الأفقية للتوقيع الرقمي. |

### setOfficeVersion(String value) {#setOfficeVersion-java.lang.String}
```
public void setOfficeVersion(String value)
```


يضبط إصدار Office للتوقيع الرقمي. القيمة الافتراضية هي "12.0".

 **Examples:** 

يعرض كيفية توقيع مستند مع خيارات توقيع إضافية.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | إصدار Office للتوقيع الرقمي. |

### setProviderId(UUID value) {#setProviderId-java.util.UUID}
```
public void setProviderId(UUID value)
```


يحدد معرف الفئة لمزود التوقيع. القيمة الافتراضية هي **Empty (all zeroes) Guid**.

 **Remarks:** 

مزود خدمة التشفير (CSP) هو وحدة برمجية مستقلة تقوم فعليًا بتنفيذ خوارزميات التشفير للمصادقة والترميز والتشفير. يحتفظ MS Office بالقيمة \\{00000000-0000-0000-0000-000000000000\\} لمزود التوقيع الافتراضي الخاص به.

يجب الحصول على GUID للمزود المثبت إضافيًا من الوثائق المرفقة مع المزود.

بالإضافة إلى ذلك، يتم تعداد جميع مزودي التشفير المثبتين في سجل Windows. يمكن العثور عليه في المسار التالي: HKLM\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider. هناك اسم مفتاح "CP Service UUID" الذي يتطابق مع GUID لمزود التوقيع.

 **Examples:** 

يعرض كيفية توقيع مستند بشهادة شخصية وسطر توقيع.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.util.UUID | القيمة المقابلة لـ java.util.UUID. |

### setSignTime(Date value) {#setSignTime-java.util.Date}
```
public void setSignTime(Date value)
```


تاريخ التوقيع. القيمة الافتراضية هي **current time**

 **Examples:** 

يعرض كيفية توقيع المستندات رقميًا.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.util.Date | القيمة المقابلة لـ java.util.Date. |

### setSignatureLineId(UUID value) {#setSignatureLineId-java.util.UUID}
```
public void setSignatureLineId(UUID value)
```


معرف سطر التوقيع. القيمة الافتراضية هي **Empty (all zeroes) Guid**.

 **Remarks:** 

عند الضبط، يربط [SignatureLine](../../com.aspose.words/signatureline/) بـ [DigitalSignature](../../com.aspose.words/digitalsignature/) المقابل.

 **Examples:** 

يعرض كيفية إضافة سطر توقيع إلى مستند، ثم توقيعه باستخدام شهادة رقمية.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.util.UUID | القيمة المقابلة لـ java.util.UUID. |

### setSignatureLineImage(byte[] value) {#setSignatureLineImage-byte}
```
public void setSignatureLineImage(byte[] value)
```


الصورة التي سيتم عرضها في [SignatureLine](../../com.aspose.words/signatureline/) المرتبط. القيمة الافتراضية هي null.

 **Examples:** 

يعرض كيفية إضافة سطر توقيع إلى مستند، ثم توقيعه باستخدام شهادة رقمية.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | byte[] | القيمة المقابلة من نوع byte[] . |

### setVerticalResolution(int value) {#setVerticalResolution-int}
```
public void setVerticalResolution(int value)
```


يضبط الدقة العمودية للتوقيع الرقمي. القيمة الافتراضية هي 1200.

 **Examples:** 

يعرض كيفية توقيع مستند مع خيارات توقيع إضافية.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | الدقة العمودية للتوقيع الرقمي. |

### setWindowsVersion(String value) {#setWindowsVersion-java.lang.String}
```
public void setWindowsVersion(String value)
```


يضبط إصدار Windows للتوقيع الرقمي. القيمة الافتراضية هي "6.1".

 **Examples:** 

يعرض كيفية توقيع مستند مع خيارات توقيع إضافية.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | إصدار Windows للتوقيع الرقمي. |

### setXmlDsigLevel(int value) {#setXmlDsigLevel-int}
```
public void setXmlDsigLevel(int value)
```


يحدد مستوى التوقيع الرقمي بناءً على معيار XML-DSig. القيمة الافتراضية هي [XmlDsigLevel.XML\_D\_SIG](../../com.aspose.words/xmldsiglevel/\#XML-D-SIG).

 **Remarks:** 

يمكن إنشاء مستويات مختلفة من توقيعات XAdES بدءًا من Office 2010.

 **Examples:** 

يعرض كيفية توقيع مستند بناءً على معيار XML-DSig.

```

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 SignOptions signOptions = new SignOptions(); { signOptions.setXmlDsigLevel(XmlDsigLevel.X_AD_ES_EPES); }

 String inputFileName = getMyDir() + "Document.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.XmlDsig.docx";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة المقابلة  int  . يجب أن تكون القيمة واحدة من ثوابت [XmlDsigLevel](../../com.aspose.words/xmldsiglevel/). |

