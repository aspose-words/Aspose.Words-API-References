---
title: "PdfDigitalSignatureDetails"
linktitle: "PdfDigitalSignatureDetails"
second_title: "Aspose.Words Java için"
description: "Java'da bir PDF belgesini dijital imza ile imzalamak için ayrıntıları içerir."
type: docs
weight: 531
url: /tr/java/com.aspose.words/pdfdigitalsignaturedetails/
---

**Inheritance:**
java.lang.Object
```
public class PdfDigitalSignatureDetails
```

Bir PDF belgesinin dijital imza ile imzalanmasıyla ilgili ayrıntıları içerir.

 **Remarks:** 

Şu anda PDF belgelerini dijital olarak imzalamak yalnızca .NET 3.5 veya üzeri sürümlerde mevcuttur.

Aspose.Words tarafından oluşturulan bir PDF belgesini dijital olarak imzalamak için, [PdfSaveOptions.getDigitalSignatureDetails()](../../com.aspose.words/pdfsaveoptions/\#getDigitalSignatureDetails) / [PdfSaveOptions.setDigitalSignatureDetails(com.aspose.words.PdfDigitalSignatureDetails)](../../com.aspose.words/pdfsaveoptions/\#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails) özelliğini geçerli bir [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails/) nesnesine ayarlayın ve ardından belgeyi PDF formatında kaydederken [PdfSaveOptions](../../com.aspose.words/pdfsaveoptions/) parametresini [Document.save(java.lang.String, com.aspose.words.SaveOptions)](../../com.aspose.words/document/\#save-java.lang.String--com.aspose.words.SaveOptions) metoduna geçirin.

Aspose.Words, tüm PDF belgesi üzerinde bir PKCS\#7 imzası oluşturur ve dijital imza oluştururken "Adobe.PPKMS" filtresi ile "adbe.pkcs7.sha1" alt filtresini kullanır.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [PdfDigitalSignatureDetails()](#PdfDigitalSignatureDetails) | Bu sınıfın bir örneğini başlatır. |
| [PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate)](#PdfDigitalSignatureDetails-com.aspose.words.CertificateHolder-java.lang.String-java.lang.String-java.util.Date) | Bu sınıfın bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür. |
| [getHashAlgorithm()](#getHashAlgorithm) | Karma algoritmasını alır. |
| [getLocation()](#getLocation) | İmzanın konumunu alır. |
| [getReason()](#getReason) | İmzanın nedenini alır. |
| [getSignatureDate()](#getSignatureDate) | İmzanın tarihini alır. |
| [getTimestampSettings()](#getTimestampSettings) | Dijital imza zaman damgası ayarlarını alır. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür. |
| [setHashAlgorithm(int value)](#setHashAlgorithm-int) | Karma algoritmasını ayarlar. |
| [setLocation(String value)](#setLocation-java.lang.String) | İmzanın konumunu ayarlar. |
| [setReason(String value)](#setReason-java.lang.String) | İmzanın nedenini ayarlar. |
| [setSignatureDate(Date value)](#setSignatureDate-java.util.Date) | İmzanın tarihini ayarlar. |
| [setTimestampSettings(PdfDigitalSignatureTimestampSettings value)](#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings) | Dijital imza zaman damgası ayarlarını ayarlar. |
### PdfDigitalSignatureDetails() {#PdfDigitalSignatureDetails}
```
public PdfDigitalSignatureDetails()
```


Bu sınıfın bir örneğini başlatır.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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


Bu sınıfın bir örneğini başlatır.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| certificateHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) | Sertifikayı kendisi içinde barındıran bir sertifika tutucu. |
| neden | java.lang.String | İmzalama nedeni. |
| konum | java.lang.String | İmzalama konumu. |
| signatureDate | java.util.Date | İmzalama tarih ve saati. |

### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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


Karma algoritmasını alır.

 **Remarks:** 

Varsayılan değer SHA-256 algoritmasıdır.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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
int - Karma algoritması. Döndürülen değer, [PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm/) sabitlerinden biridir.
### getLocation() {#getLocation}
```
public String getLocation()
```


İmzanın konumunu alır.

 **Remarks:** 

Varsayılan değer  null  dır.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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
java.lang.String - İmzalamanın konumu.
### getReason() {#getReason}
```
public String getReason()
```


İmzanın nedenini alır.

 **Remarks:** 

Varsayılan değer  null  dır.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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
java.lang.String - İmzalamanın nedeni.
### getSignatureDate() {#getSignatureDate}
```
public Date getSignatureDate()
```


İmzanın tarihini alır.

 **Remarks:** 

Varsayılan değer geçerli zamandır.

Bu değer, dijital imzada doğrulanmamış bir bilgisayar zamanı olarak görünecektir.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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
java.util.Date - İmzalamanın tarihi.
### getTimestampSettings() {#getTimestampSettings}
```
public PdfDigitalSignatureTimestampSettings getTimestampSettings()
```


Dijital imza zaman damgası ayarlarını alır.

 **Remarks:** 

Varsayılan değer  null  ve dijital imza zaman damgası eklenmez. Bu özellik geçerli bir [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) nesnesine ayarlandığında, PDF belgesindeki dijital imza zaman damgası alır.

 **Examples:** 

Kaydedilmiş bir PDF belgesinin dijital olarak nasıl imzalanacağını ve zaman damgası ekleneceğini gösterir.

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


Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | Belgeyi imzalamak için kullanılan, sertifikayı içeren sertifika sahibi nesnesi. |

### setHashAlgorithm(int value) {#setHashAlgorithm-int}
```
public void setHashAlgorithm(int value)
```


Karma algoritmasını ayarlar.

 **Remarks:** 

Varsayılan değer SHA-256 algoritmasıdır.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Karma algoritması. Değer, [PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm/) sabitlerinden biri olmalıdır. |

### setLocation(String value) {#setLocation-java.lang.String}
```
public void setLocation(String value)
```


İmzanın konumunu ayarlar.

 **Remarks:** 

Varsayılan değer  null  dır.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İmzalamanın konumu. |

### setReason(String value) {#setReason-java.lang.String}
```
public void setReason(String value)
```


İmzanın nedenini ayarlar.

 **Remarks:** 

Varsayılan değer  null  dır.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İmzalamanın nedeni. |

### setSignatureDate(Date value) {#setSignatureDate-java.util.Date}
```
public void setSignatureDate(Date value)
```


İmzanın tarihini ayarlar.

 **Remarks:** 

Varsayılan değer geçerli zamandır.

Bu değer, dijital imzada doğrulanmamış bir bilgisayar zamanı olarak görünecektir.

 **Examples:** 

Oluşturulan bir PDF belgesini imzalamanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.util.Date | İmzalamanın tarihi. |

### setTimestampSettings(PdfDigitalSignatureTimestampSettings value) {#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings}
```
public void setTimestampSettings(PdfDigitalSignatureTimestampSettings value)
```


Dijital imza zaman damgası ayarlarını ayarlar.

 **Remarks:** 

Varsayılan değer  null  ve dijital imza zaman damgası eklenmez. Bu özellik geçerli bir [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) nesnesine ayarlandığında, PDF belgesindeki dijital imza zaman damgası alır.

 **Examples:** 

Kaydedilmiş bir PDF belgesinin dijital olarak nasıl imzalanacağını ve zaman damgası ekleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) | Dijital imza zaman damgası ayarları. |

