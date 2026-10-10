---
title: "PdfDigitalSignatureDetails"
linktitle: "PdfDigitalSignatureDetails"
second_title: "Aspose.Words لـ Java"
description: "يحتوي على تفاصيل توقيع مستند PDF بتوقيع رقمي في Java."
type: docs
weight: 531
url: /ar/java/com.aspose.words/pdfdigitalsignaturedetails/
---

**Inheritance:**
java.lang.Object
```
public class PdfDigitalSignatureDetails
```

يحتوي على تفاصيل توقيع مستند PDF بتوقيع رقمي.

 **Remarks:** 

في الوقت الحالي، توقيع مستندات PDF رقمياً متاح فقط على .NET 3.5 أو أعلى.

لتوقيع مستند PDF رقمياً عندما يتم إنشاؤه بواسطة Aspose.Words، اضبط الخاصية [PdfSaveOptions.getDigitalSignatureDetails()](../../com.aspose.words/pdfsaveoptions/\#getDigitalSignatureDetails) / [PdfSaveOptions.setDigitalSignatureDetails(com.aspose.words.PdfDigitalSignatureDetails)](../../com.aspose.words/pdfsaveoptions/\#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails) إلى كائن [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails/) صالح ثم احفظ المستند بتنسيق PDF مع تمرير [PdfSaveOptions](../../com.aspose.words/pdfsaveoptions/) كمعامل إلى طريقة [Document.save(java.lang.String, com.aspose.words.SaveOptions)](../../com.aspose.words/document/\#save-java.lang.String--com.aspose.words.SaveOptions).

تنشئ Aspose.Words توقيع PKCS\#7 على كامل مستند PDF وتستخدم الفلتر \"Adobe.PPKMS\" والفلتر الفرعي \"adbe.pkcs7.sha1\" عند إنشاء توقيع رقمي.

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [PdfDigitalSignatureDetails()](#PdfDigitalSignatureDetails) | يقوم بتهيئة نسخة من هذه الفئة. |
| [PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate)](#PdfDigitalSignatureDetails-com.aspose.words.CertificateHolder-java.lang.String-java.lang.String-java.util.Date) | يقوم بتهيئة نسخة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | يعيد كائن حامل الشهادة الذي يحتوي على الشهادة المستخدمة لتوقيع المستند. |
| [getHashAlgorithm()](#getHashAlgorithm) | يحصل على خوارزمية التجزئة. |
| [getLocation()](#getLocation) | يحصل على موقع التوقيع. |
| [getReason()](#getReason) | يحصل على سبب التوقيع. |
| [getSignatureDate()](#getSignatureDate) | يحصل على تاريخ التوقيع. |
| [getTimestampSettings()](#getTimestampSettings) | يحصل على إعدادات طابع الوقت للتوقيع الرقمي. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | يعيد كائن حامل الشهادة الذي يحتوي على الشهادة المستخدمة لتوقيع المستند. |
| [setHashAlgorithm(int value)](#setHashAlgorithm-int) | يضبط خوارزمية التجزئة. |
| [setLocation(String value)](#setLocation-java.lang.String) | يضبط موقع التوقيع. |
| [setReason(String value)](#setReason-java.lang.String) | يضبط سبب التوقيع. |
| [setSignatureDate(Date value)](#setSignatureDate-java.util.Date) | يضبط تاريخ التوقيع. |
| [setTimestampSettings(PdfDigitalSignatureTimestampSettings value)](#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings) | يضبط إعدادات طابع الوقت للتوقيع الرقمي. |
### PdfDigitalSignatureDetails() {#PdfDigitalSignatureDetails}
```
public PdfDigitalSignatureDetails()
```


يقوم بتهيئة نسخة من هذه الفئة.

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```

### PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate) {#PdfDigitalSignatureDetails-com.aspose.words.CertificateHolder-java.lang.String-java.lang.String-java.util.Date}
```
public PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate)
```


يقوم بتهيئة نسخة من هذه الفئة.

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| certificateHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) | حامل شهادة يحتوي على الشهادة نفسها. |
| السبب | java.lang.String | السبب للتوقيع. |
| الموقع | java.lang.String | موقع التوقيع. |
| signatureDate | java.util.Date | التاريخ والوقت للتوقيع. |

### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


يعيد كائن حامل الشهادة الذي يحتوي على الشهادة المستخدمة لتوقيع المستند.

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The certificate holder object that contains the certificate was used to sign the document.
### getHashAlgorithm() {#getHashAlgorithm}
```
public int getHashAlgorithm()
```


يحصل على خوارزمية التجزئة.

 **Remarks:** 

القيمة الافتراضية هي خوارزمية SHA-256.

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```

**Returns:**
int - خوارزمية التجزئة. القيمة المرجعة هي واحدة من ثوابت [PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm/).
### getLocation() {#getLocation}
```
public String getLocation()
```


يحصل على موقع التوقيع.

 **Remarks:** 

القيمة الافتراضية هي  null .

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```

**Returns:**
java.lang.String - موقع التوقيع.
### getReason() {#getReason}
```
public String getReason()
```


يحصل على سبب التوقيع.

 **Remarks:** 

القيمة الافتراضية هي  null .

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```

**Returns:**
java.lang.String - سبب التوقيع.
### getSignatureDate() {#getSignatureDate}
```
public Date getSignatureDate()
```


يحصل على تاريخ التوقيع.

 **Remarks:** 

القيمة الافتراضية هي الوقت الحالي.

ستظهر هذه القيمة في التوقيع الرقمي كوقت حاسوب غير موثوق به.

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```

**Returns:**
java.util.Date - تاريخ التوقيع.
### getTimestampSettings() {#getTimestampSettings}
```
public PdfDigitalSignatureTimestampSettings getTimestampSettings()
```


يحصل على إعدادات طابع الوقت للتوقيع الرقمي.

 **Remarks:** 

القيمة الافتراضية هي  null  ولن يتم وضع طابع زمني على التوقيع الرقمي. عندما يتم تعيين هذه الخاصية إلى كائن [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) صالح، سيتم وضع طابع زمني على التوقيع الرقمي في مستند PDF.

 **Examples:** 

يوضح كيفية توقيع مستند PDF محفوظ رقمياً وإضافة طابع وقت له.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Signed PDF contents.");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Create a digital signature and assign it to our SaveOptions object to sign the document when we save it to PDF.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", new Date()));

 // Create a timestamp authority-verified timestamp.
 options.getDigitalSignatureDetails().setTimestampSettings(new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword"));

 // The default lifespan of the timestamp is 100 seconds.
 Assert.assertEquals(options.getDigitalSignatureDetails().getTimestampSettings().getTimeout(), 100000);

 // We can set our own timeout period via the constructor.
 options.getDigitalSignatureDetails().setTimestampSettings(new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", (long) 1800.0));

 Assert.assertEquals(options.getDigitalSignatureDetails().getTimestampSettings().getTimeout(), 1800);
 Assert.assertEquals(options.getDigitalSignatureDetails().getTimestampSettings().getServerUrl(), "https://freetsa.org/tsr");
 Assert.assertEquals(options.getDigitalSignatureDetails().getTimestampSettings().getUserName(), "JohnDoe");
 Assert.assertEquals(options.getDigitalSignatureDetails().getTimestampSettings().getPassword(), "MyPassword");

 // The "Save" method will apply our signature to the output document at this time.
 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
 
```

**Returns:**
[PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) - The digital signature timestamp settings.
### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder}
```
public void setCertificateHolder(CertificateHolder value)
```


يعيد كائن حامل الشهادة الذي يحتوي على الشهادة المستخدمة لتوقيع المستند.

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | تم استخدام كائن حامل الشهادة الذي يحتوي على الشهادة لتوقيع المستند. |

### setHashAlgorithm(int value) {#setHashAlgorithm-int}
```
public void setHashAlgorithm(int value)
```


يضبط خوارزمية التجزئة.

 **Remarks:** 

القيمة الافتراضية هي خوارزمية SHA-256.

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | خوارزمية التجزئة. يجب أن تكون القيمة واحدة من ثوابت [PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm/). |

### setLocation(String value) {#setLocation-java.lang.String}
```
public void setLocation(String value)
```


يضبط موقع التوقيع.

 **Remarks:** 

القيمة الافتراضية هي  null .

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | موقع التوقيع. |

### setReason(String value) {#setReason-java.lang.String}
```
public void setReason(String value)
```


يضبط سبب التوقيع.

 **Remarks:** 

القيمة الافتراضية هي  null .

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | سبب التوقيع. |

### setSignatureDate(Date value) {#setSignatureDate-java.util.Date}
```
public void setSignatureDate(Date value)
```


يضبط تاريخ التوقيع.

 **Remarks:** 

القيمة الافتراضية هي الوقت الحالي.

ستظهر هذه القيمة في التوقيع الرقمي كوقت حاسوب غير موثوق به.

 **Examples:** 

يعرض كيفية توقيع مستند PDF مُولد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Contents of signed PDF.");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
 // digitally sign the document as we render it with the "Save" method.
 Calendar calendar = Calendar.getInstance();
 calendar.set(2015, Calendar.JULY, 20);
 Date signingTime = calendar.getTime();
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "My Office", signingTime));
 options.getDigitalSignatureDetails().setHashAlgorithm(PdfDigitalSignatureHashAlgorithm.RIPE_MD_160);

 Assert.assertEquals(options.getDigitalSignatureDetails().getReason(), "Test Signing");
 Assert.assertEquals(options.getDigitalSignatureDetails().getLocation(), "My Office");
 Assert.assertEquals(DocumentHelper.getLocalDate(options.getDigitalSignatureDetails().getSignatureDate()), DocumentHelper.getLocalDate(signingTime));

 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignature.pdf", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.util.Date | تاريخ التوقيع. |

### setTimestampSettings(PdfDigitalSignatureTimestampSettings value) {#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings}
```
public void setTimestampSettings(PdfDigitalSignatureTimestampSettings value)
```


يضبط إعدادات طابع الوقت للتوقيع الرقمي.

 **Remarks:** 

القيمة الافتراضية هي  null  ولن يتم وضع طابع زمني على التوقيع الرقمي. عندما يتم تعيين هذه الخاصية إلى كائن [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) صالح، سيتم وضع طابع زمني على التوقيع الرقمي في مستند PDF.

 **Examples:** 

يوضح كيفية توقيع مستند PDF محفوظ رقمياً وإضافة طابع وقت له.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Signed PDF contents.");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Create a digital signature and assign it to our SaveOptions object to sign the document when we save it to PDF.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");
 options.setDigitalSignatureDetails(new PdfDigitalSignatureDetails(certificateHolder, "Test Signing", "Aspose Office", new Date()));

 // Create a timestamp authority-verified timestamp.
 options.getDigitalSignatureDetails().setTimestampSettings(new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword"));

 // The default lifespan of the timestamp is 100 seconds.
 Assert.assertEquals(options.getDigitalSignatureDetails().getTimestampSettings().getTimeout(), 100000);

 // We can set our own timeout period via the constructor.
 options.getDigitalSignatureDetails().setTimestampSettings(new PdfDigitalSignatureTimestampSettings("https://freetsa.org/tsr", "JohnDoe", "MyPassword", (long) 1800.0));

 Assert.assertEquals(options.getDigitalSignatureDetails().getTimestampSettings().getTimeout(), 1800);
 Assert.assertEquals(options.getDigitalSignatureDetails().getTimestampSettings().getServerUrl(), "https://freetsa.org/tsr");
 Assert.assertEquals(options.getDigitalSignatureDetails().getTimestampSettings().getUserName(), "JohnDoe");
 Assert.assertEquals(options.getDigitalSignatureDetails().getTimestampSettings().getPassword(), "MyPassword");

 // The "Save" method will apply our signature to the output document at this time.
 doc.save(getArtifactsDir() + "PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) | إعدادات طابع توقيع الرقمي. |

