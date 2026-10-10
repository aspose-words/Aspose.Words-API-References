---
title: "DigitalSignature"
linktitle: "DigitalSignature"
second_title: "Aspose.Words لـ Java"
description: "يمثل توقيعًا رقميًا على مستند ونتيجة التحقق منه في Java."
type: docs
weight: 150
url: /ar/java/com.aspose.words/digitalsignature/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignature
```

يمثل توقيعًا رقميًا على مستند ونتيجة التحقق منه.

لمزيد من المعلومات، زر مقالة الوثائق [ Work with Digital Signatures ][Work with Digital Signatures].

 **Examples:** 

يعرض كيفية التحقق وعرض المعلومات حول كل توقيع في وثيقة.

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


[Work with Digital Signatures]: https://docs.aspose.com/words/java/working-with-digital-signatures/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getApplicationVersion()](#getApplicationVersion) | يحصل على إصدار التطبيق للتوقيع الرقمي. |
| [getCertificateHolder()](#getCertificateHolder) | يعيد كائن حامل الشهادة الذي يحتوي على الشهادة المستخدمة لتوقيع المستند. |
| [getColorDepth()](#getColorDepth) | يحصل على عمق اللون للتوقيع الرقمي. |
| [getComments()](#getComments) | يحصل على تعليق هدف التوقيع. |
| [getHorizontalResolution()](#getHorizontalResolution) | يحصل على الدقة الأفقية للتوقيع الرقمي. |
| [getIssuerName()](#getIssuerName) | يعيد الاسم المميز للموضوع للجهة المصدرة للشهادة. |
| [getOfficeVersion()](#getOfficeVersion) | يحصل على إصدار Office للتوقيع الرقمي. |
| [getSignTime()](#getSignTime) | يحصل على وقت توقيع المستند. |
| [getSignatureType()](#getSignatureType) | يحصل على نوع التوقيع الرقمي. |
| [getSignatureValue()](#getSignatureValue) | يحصل على مصفوفة من البايتات تمثل قيمة التوقيع. |
| [getSubjectName()](#getSubjectName) | يعيد الاسم المميز للموضوع في الشهادة التي تم استخدامها لتوقيع المستند. |
| [getVerticalResolution()](#getVerticalResolution) | يحصل على الدقة العمودية للتوقيع الرقمي. |
| [getWindowsVersion()](#getWindowsVersion) | يحصل على إصدار Windows للتوقيع الرقمي. |
| [isValid()](#isValid) | يعيد  true  إذا كان هذا التوقيع الرقمي صالحًا ولم يتم العبث بالمستند. |
| [toString()](#toString) | يعيد سلسلة سهلة القراءة تعرض قيمة هذا الكائن. |
### getApplicationVersion() {#getApplicationVersion}
```
public String getApplicationVersion()
```


يحصل على إصدار التطبيق للتوقيع الرقمي.

**Returns:**
java.lang.String - إصدار التطبيق للتوقيع الرقمي.
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


يعيد كائن حامل الشهادة الذي يحتوي على الشهادة المستخدمة لتوقيع المستند.

 **Examples:** 

يعرض كيفية توقيع المستندات باستخدام شهادات X.509.

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

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The certificate holder object that contains the certificate was used to sign the document.
### getColorDepth() {#getColorDepth}
```
public int getColorDepth()
```


يحصل على عمق اللون للتوقيع الرقمي.

**Returns:**
int - عمق اللون للتوقيع الرقمي.
### getComments() {#getComments}
```
public String getComments()
```


يحصل على تعليق هدف التوقيع.

 **Examples:** 

يعرض كيفية التحقق وعرض المعلومات حول كل توقيع في وثيقة.

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
java.lang.String - تعليق هدف التوقيع.
### getHorizontalResolution() {#getHorizontalResolution}
```
public int getHorizontalResolution()
```


يحصل على الدقة الأفقية للتوقيع الرقمي.

**Returns:**
int - الدقة الأفقية للتوقيع الرقمي.
### getIssuerName() {#getIssuerName}
```
public String getIssuerName()
```


يعيد الاسم المميز للموضوع للجهة المصدرة للشهادة.

 **Examples:** 

يعرض كيفية توقيع المستندات باستخدام شهادات X.509.

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

**Returns:**
java.lang.String - الاسم المميز للموضوع في شهادة المصدر.
### getOfficeVersion() {#getOfficeVersion}
```
public String getOfficeVersion()
```


يحصل على إصدار Office للتوقيع الرقمي.

**Returns:**
java.lang.String - إصدار Office للتوقيع الرقمي.
### getSignTime() {#getSignTime}
```
public Date getSignTime()
```


يحصل على وقت توقيع المستند.

 **Examples:** 

يعرض كيفية التحقق وعرض المعلومات حول كل توقيع في وثيقة.

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
java.util.Date - الوقت الذي تم توقيع المستند فيه.
### getSignatureType() {#getSignatureType}
```
public int getSignatureType()
```


يحصل على نوع التوقيع الرقمي.

 **Examples:** 

يعرض كيفية التحقق وعرض المعلومات حول كل توقيع في وثيقة.

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
int - نوع التوقيع الرقمي. القيمة المعادة هي واحدة من ثوابت [DigitalSignatureType](../../com.aspose.words/digitalsignaturetype/).
### getSignatureValue() {#getSignatureValue}
```
public byte[] getSignatureValue()
```


يحصل على مصفوفة من البايتات تمثل قيمة التوقيع.

 **Examples:** 

يوضح كيفية الحصول على قيمة توقيع رقمي من مستند موقع رقمياً.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature digitalSignature : doc.getDigitalSignatures())
 {
     String signatureValue = Base64.getEncoder().encodeToString(digitalSignature.getSignatureValue());
     Assert.assertEquals("K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbD" +
             "MhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm" +
             "+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=", signatureValue);
 }
 
```

**Returns:**
byte[] - مصفوفة من البايتات تمثل قيمة التوقيع.
### getSubjectName() {#getSubjectName}
```
public String getSubjectName()
```


يعيد الاسم المميز للموضوع في الشهادة التي تم استخدامها لتوقيع المستند.

 **Examples:** 

يعرض كيفية توقيع المستندات باستخدام شهادات X.509.

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

**Returns:**
java.lang.String - الاسم المميز للموضوع في الشهادة التي تم استخدامها لتوقيع المستند.
### getVerticalResolution() {#getVerticalResolution}
```
public int getVerticalResolution()
```


يحصل على الدقة العمودية للتوقيع الرقمي.

**Returns:**
int - الدقة العمودية للتوقيع الرقمي.
### getWindowsVersion() {#getWindowsVersion}
```
public String getWindowsVersion()
```


يحصل على إصدار Windows للتوقيع الرقمي.

**Returns:**
java.lang.String - إصدار Windows للتوقيع الرقمي.
### isValid() {#isValid}
```
public boolean isValid()
```


يعيد  true  إذا كان هذا التوقيع الرقمي صالحًا ولم يتم العبث بالمستند.

 **Examples:** 

يعرض كيفية التحقق وعرض المعلومات حول كل توقيع في وثيقة.

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
boolean -  true  إذا كان هذا التوقيع الرقمي صالحًا ولم يتم العبث بالمستند.
### toString() {#toString}
```
public String toString()
```


يعيد سلسلة سهلة القراءة تعرض قيمة هذا الكائن.

**Returns:**
java.lang.String
