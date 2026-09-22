---
title: "SignatureLine"
linktitle: "SignatureLine"
second_title: "Aspose.Words لـ Java"
description: "يوفر الوصول إلى خصائص سطر التوقيع في Java."
type: docs
weight: 621
url: /ar/java/com.aspose.words/signatureline/
---

**Inheritance:**
java.lang.Object
```
public class SignatureLine
```

يوفر الوصول إلى خصائص سطر التوقيع.

لمزيد من المعلومات، زر مقالة الوثائق [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAllowComments()](#getAllowComments) | يحصل على قيمة تشير إلى أن الموقّع يمكنه إضافة تعليقات في مربع حوار التوقيع. |
| [getDefaultInstructions()](#getDefaultInstructions) | يحصل على قيمة تشير إلى أن التعليمات الافتراضية تُعرض في مربع حوار التوقيع. |
| [getEmail()](#getEmail) | يحصل على عنوان البريد الإلكتروني المقترح للموقع. |
| [getId()](#getId) | يحصل على المعرف لهذا سطر التوقيع. |
| [getInstructions()](#getInstructions) | يحصل على التعليمات للموقع التي تُعرض عند توقيع سطر التوقيع. |
| [getProviderId()](#getProviderId) | يحصل على معرف موفر التوقيع لهذا سطر التوقيع. |
| [getShowDate()](#getShowDate) | يحصل على قيمة تشير إلى أن تاريخ التوقيع يُعرض في سطر التوقيع. |
| [getSigner()](#getSigner) | يحصل على اسم الموقع المقترح لسطر التوقيع. |
| [getSignerTitle()](#getSignerTitle) | يحصل على لقب المُوقّع المقترح (مثلاً، مدير). |
| [isSigned()](#isSigned) | يشير إلى أن سطر التوقيع موقع بتوقيع رقمي. |
| [isValid()](#isValid) | يشير إلى أن سطر التوقيع موقع بتوقيع رقمي وأن هذا التوقيع الرقمي صالح. |
| [setAllowComments(boolean value)](#setAllowComments-boolean) | يضبط قيمة تشير إلى أن الموقع يمكنه إضافة تعليقات في مربع حوار التوقيع. |
| [setDefaultInstructions(boolean value)](#setDefaultInstructions-boolean) | يضبط قيمة تشير إلى أن التعليمات الافتراضية تُعرض في مربع حوار التوقيع. |
| [setEmail(String value)](#setEmail-java.lang.String) | يضبط عنوان البريد الإلكتروني المقترح للموقع. |
| [setId(UUID value)](#setId-java.util.UUID) | يضبط المعرف لهذا سطر التوقيع. |
| [setInstructions(String value)](#setInstructions-java.lang.String) | يضبط التعليمات للموقع التي تُعرض عند توقيع سطر التوقيع. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID) | يضبط معرف موفر التوقيع لهذا سطر التوقيع. |
| [setShowDate(boolean value)](#setShowDate-boolean) | يضبط قيمة تشير إلى أن تاريخ التوقيع يُعرض في سطر التوقيع. |
| [setSigner(String value)](#setSigner-java.lang.String) | يضبط اسم الموقع المقترح لسطر التوقيع. |
| [setSignerTitle(String value)](#setSignerTitle-java.lang.String) | يضبط لقب المُوقّع المقترح (مثلاً، مدير). |
### getAllowComments() {#getAllowComments}
```
public boolean getAllowComments()
```


يحصل على قيمة تشير إلى أن الموقع يمكنه إضافة تعليقات في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي false.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
منطقية - قيمة تشير إلى أن الموقع يمكنه إضافة تعليقات في مربع حوار التوقيع.
### getDefaultInstructions() {#getDefaultInstructions}
```
public boolean getDefaultInstructions()
```


يحصل على قيمة تشير إلى أن التعليمات الافتراضية تُعرض في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي true.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
منطقية - قيمة تشير إلى أن التعليمات الافتراضية تُعرض في مربع حوار التوقيع.
### getEmail() {#getEmail}
```
public String getEmail()
```


يحصل على عنوان البريد الإلكتروني المقترح للموقع. القيمة الافتراضية لهذه الخاصية هي **empty string**.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
java.lang.String - عنوان البريد الإلكتروني المقترح للموقع.
### getId() {#getId}
```
public UUID getId()
```


يحصل على المعرف لهذا سطر التوقيع.

يمكن ربط هذا المعرف بتوقيع رقمي، عند توقيع المستند باستخدام [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil/). يجب أن تكون هذه القيمة فريدة وبشكل افتراضي يتم توليد GUID جديد عشوائيًا.

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
java.util.UUID - المعرف لهذا سطر التوقيع.
### getInstructions() {#getInstructions}
```
public String getInstructions()
```


يحصل على التعليمات للموقع التي تُعرض عند توقيع سطر التوقيع. يتم تجاهل هذه الخاصية إذا تم تعيين [getDefaultInstructions()](../../com.aspose.words/signatureline/\#getDefaultInstructions) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline/\#setDefaultInstructions-boolean). القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة**.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
java.lang.String - التعليمات للموقع التي تُعرض عند توقيع سطر التوقيع.
### getProviderId() {#getProviderId}
```
public UUID getProviderId()
```


يحصل على معرف موفر التوقيع لهذا سطر التوقيع. القيمة الافتراضية هي "{00000000-0000-0000-0000-000000000000}".

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
java.util.UUID - معرف موفر التوقيع لهذا سطر التوقيع.
### getShowDate() {#getShowDate}
```
public boolean getShowDate()
```


يحصل على قيمة تشير إلى أن تاريخ التوقيع يُعرض في سطر التوقيع. القيمة الافتراضية لهذه الخاصية هي true.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
منطقية - قيمة تشير إلى أن تاريخ التوقيع يُعرض في سطر التوقيع.
### getSigner() {#getSigner}
```
public String getSigner()
```


يحصل على اسم الموقع المقترح لسطر التوقيع. القيمة الافتراضية لهذه الخاصية هي **empty string**.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
java.lang.String - اسم الموقع المقترح لسطر التوقيع.
### getSignerTitle() {#getSignerTitle}
```
public String getSignerTitle()
```


يحصل على لقب الموقع المقترح (على سبيل المثال، مدير). القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة**.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
java.lang.String - لقب الموقع المقترح (على سبيل المثال، مدير).
### isSigned() {#isSigned}
```
public boolean isSigned()
```


يشير إلى أن سطر التوقيع موقع بتوقيع رقمي.

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
boolean - القيمة المنطقية المقابلة.
### isValid() {#isValid}
```
public boolean isValid()
```


يشير إلى أن سطر التوقيع موقع بتوقيع رقمي وأن هذا التوقيع الرقمي صالح.

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
boolean - القيمة المنطقية المقابلة.
### setAllowComments(boolean value) {#setAllowComments-boolean}
```
public void setAllowComments(boolean value)
```


يضبط قيمة تشير إلى أن المُوقّع يمكنه إضافة تعليقات في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي false.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تشير إلى أن المُوقّع يمكنه إضافة تعليقات في مربع حوار التوقيع. |

### setDefaultInstructions(boolean value) {#setDefaultInstructions-boolean}
```
public void setDefaultInstructions(boolean value)
```


يضبط قيمة تشير إلى أن التعليمات الافتراضية تُعرض في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي true.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تشير إلى أن التعليمات الافتراضية تُعرض في مربع حوار التوقيع. |

### setEmail(String value) {#setEmail-java.lang.String}
```
public void setEmail(String value)
```


يضبط عنوان البريد الإلكتروني المقترح للمُوقّع. القيمة الافتراضية لهذه الخاصية هي **empty string**.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | عنوان البريد الإلكتروني المقترح للمُوقّع. |

### setId(UUID value) {#setId-java.util.UUID}
```
public void setId(UUID value)
```


يضبط المعرف لهذا سطر التوقيع.

يمكن ربط هذا المعرف بتوقيع رقمي، عند توقيع المستند باستخدام [DigitalSignatureUtil](../../com.aspose.words/digitalsignatureutil/). يجب أن تكون هذه القيمة فريدة وبشكل افتراضي يتم توليد GUID جديد عشوائيًا.

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
| قيمة | java.util.UUID | المعرف لهذا سطر التوقيع. |

### setInstructions(String value) {#setInstructions-java.lang.String}
```
public void setInstructions(String value)
```


يضبط التعليمات للموقع التي تُعرض عند توقيع سطر التوقيع. يتم تجاهل هذه الخاصية إذا تم تعيين [getDefaultInstructions()](../../com.aspose.words/signatureline/\#getDefaultInstructions) / [setDefaultInstructions(boolean)](../../com.aspose.words/signatureline/\#setDefaultInstructions-boolean). القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة**.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | التعليمات للمُوقّع التي تُعرض عند توقيع سطر التوقيع. |

### setProviderId(UUID value) {#setProviderId-java.util.UUID}
```
public void setProviderId(UUID value)
```


يضبط معرف موفر التوقيع لهذا سطر التوقيع. القيمة الافتراضية هي "{00000000-0000-0000-0000-000000000000}".

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
| قيمة | java.util.UUID | معرف موفر التوقيع لهذا سطر التوقيع. |

### setShowDate(boolean value) {#setShowDate-boolean}
```
public void setShowDate(boolean value)
```


يضبط قيمة تشير إلى أن تاريخ التوقيع يُعرض في سطر التوقيع. القيمة الافتراضية لهذه الخاصية هي true.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة تشير إلى أن تاريخ التوقيع يُعرض في سطر التوقيع. |

### setSigner(String value) {#setSigner-java.lang.String}
```
public void setSigner(String value)
```


يضبط المُوقّع المقترح لسطر التوقيع. القيمة الافتراضية لهذه الخاصية هي **empty string**.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | المُوقّع المقترح لسطر التوقيع. |

### setSignerTitle(String value) {#setSignerTitle-java.lang.String}
```
public void setSignerTitle(String value)
```


يضبط لقب الموقع المقترح (على سبيل المثال، مدير). القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة**.

 **Examples:** 

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | لقب الموقع المقترح (على سبيل المثال، مدير). |

