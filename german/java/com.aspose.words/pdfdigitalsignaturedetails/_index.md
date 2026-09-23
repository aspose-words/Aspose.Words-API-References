---
title: "PdfDigitalSignatureDetails"
linktitle: "PdfDigitalSignatureDetails"
second_title: "Aspose.Words für Java"
description: "Enthält Details zum Signieren eines PDF-Dokuments mit einer digitalen Signatur in Java."
type: docs
weight: 531
url: /de/java/com.aspose.words/pdfdigitalsignaturedetails/
---

**Inheritance:**
java.lang.Object
```
public class PdfDigitalSignatureDetails
```

Enthält Details zum Signieren eines PDF-Dokuments mit einer digitalen Signatur.

 **Remarks:** 

Derzeit ist das digitale Signieren von PDF-Dokumenten nur unter .NET 3.5 oder höher verfügbar.

Um ein PDF-Dokument digital zu signieren, wenn es von Aspose.Words erstellt wird, setzen Sie die Eigenschaft [PdfSaveOptions.getDigitalSignatureDetails()](../../com.aspose.words/pdfsaveoptions/\#getDigitalSignatureDetails) / [PdfSaveOptions.setDigitalSignatureDetails(com.aspose.words.PdfDigitalSignatureDetails)](../../com.aspose.words/pdfsaveoptions/\#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails) auf ein gültiges [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails/) Objekt und speichern dann das Dokument im PDF-Format, indem Sie die [PdfSaveOptions](../../com.aspose.words/pdfsaveoptions/) als Parameter an die Methode [Document.save(java.lang.String, com.aspose.words.SaveOptions)](../../com.aspose.words/document/\#save-java.lang.String--com.aspose.words.SaveOptions) übergeben.

Aspose.Words erstellt eine PKCS\#7-Signatur über das gesamte PDF-Dokument und verwendet beim Erstellen einer digitalen Signatur den Filter \"Adobe.PPKMS\" sowie den Subfilter \"adbe.pkcs7.sha1\".

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [PdfDigitalSignatureDetails()](#PdfDigitalSignatureDetails) | Initialisiert eine Instanz dieser Klasse. |
| [PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate)](#PdfDigitalSignatureDetails-com.aspose.words.CertificateHolder-java.lang.String-java.lang.String-java.util.Date) | Initialisiert eine Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | Gibt das Zertifikatsinhaber-Objekt zurück, das das Zertifikat enthält, das zum Signieren des Dokuments verwendet wurde. |
| [getHashAlgorithm()](#getHashAlgorithm) | Liefert den Hash-Algorithmus. |
| [getLocation()](#getLocation) | Liefert den Ort der Signatur. |
| [getReason()](#getReason) | Liefert den Grund der Signatur. |
| [getSignatureDate()](#getSignatureDate) | Liefert das Datum der Signatur. |
| [getTimestampSettings()](#getTimestampSettings) | Liefert die Einstellungen für den Zeitstempel der digitalen Signatur. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | Gibt das Zertifikatsinhaber-Objekt zurück, das das Zertifikat enthält, das zum Signieren des Dokuments verwendet wurde. |
| [setHashAlgorithm(int value)](#setHashAlgorithm-int) | Setzt den Hash-Algorithmus. |
| [setLocation(String value)](#setLocation-java.lang.String) | Setzt den Ort der Signatur. |
| [setReason(String value)](#setReason-java.lang.String) | Setzt den Grund der Signatur. |
| [setSignatureDate(Date value)](#setSignatureDate-java.util.Date) | Setzt das Datum der Signatur. |
| [setTimestampSettings(PdfDigitalSignatureTimestampSettings value)](#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings) | Setzt die Einstellungen für den Zeitstempel der digitalen Signatur. |
### PdfDigitalSignatureDetails() {#PdfDigitalSignatureDetails}
```
public PdfDigitalSignatureDetails()
```


Initialisiert eine Instanz dieser Klasse.

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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


Initialisiert eine Instanz dieser Klasse.

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| certificateHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) | Ein Zertifikatsinhaber, der das Zertifikat selbst enthält. |
| reason | java.lang.String | Der Grund für die Signatur. |
| location | java.lang.String | Der Ort der Signatur. |
| signatureDate | java.util.Date | Datum und Uhrzeit der Signatur. |

### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Gibt das Zertifikatsinhaber-Objekt zurück, das das Zertifikat enthält, das zum Signieren des Dokuments verwendet wurde.

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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


Liefert den Hash-Algorithmus.

 **Remarks:** 

Der Standardwert ist der SHA-256-Algorithmus.

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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
int - Der Hash-Algorithmus. Der zurückgegebene Wert ist einer der Konstanten von [PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm/).
### getLocation() {#getLocation}
```
public String getLocation()
```


Liefert den Ort der Signatur.

 **Remarks:** 

Der Standardwert ist  null .

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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
java.lang.String - Der Ort der Signatur.
### getReason() {#getReason}
```
public String getReason()
```


Liefert den Grund der Signatur.

 **Remarks:** 

Der Standardwert ist  null .

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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
java.lang.String - Der Grund für die Signatur.
### getSignatureDate() {#getSignatureDate}
```
public Date getSignatureDate()
```


Liefert das Datum der Signatur.

 **Remarks:** 

Der Standardwert ist die aktuelle Zeit.

Dieser Wert wird in der digitalen Signatur als nicht verifizierte Computerzeit angezeigt.

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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
java.util.Date - Das Datum der Signatur.
### getTimestampSettings() {#getTimestampSettings}
```
public PdfDigitalSignatureTimestampSettings getTimestampSettings()
```


Liefert die Einstellungen für den Zeitstempel der digitalen Signatur.

 **Remarks:** 

Der Standardwert ist  null  und die digitale Signatur wird nicht mit einem Zeitstempel versehen. Wenn diese Eigenschaft auf ein gültiges [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) Objekt gesetzt wird, dann wird die digitale Signatur im PDF-Dokument mit einem Zeitstempel versehen.

 **Examples:** 

Zeigt, wie ein gespeichertes PDF-Dokument digital signiert und mit einem Zeitstempel versehen wird.

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


Gibt das Zertifikatsinhaber-Objekt zurück, das das Zertifikat enthält, das zum Signieren des Dokuments verwendet wurde.

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | Das Zertifikatsinhaber-Objekt, das das Zertifikat enthält, wurde verwendet, um das Dokument zu signieren. |

### setHashAlgorithm(int value) {#setHashAlgorithm-int}
```
public void setHashAlgorithm(int value)
```


Setzt den Hash-Algorithmus.

 **Remarks:** 

Der Standardwert ist der SHA-256-Algorithmus.

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der Hash-Algorithmus. Der Wert muss einer der [PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm/) Konstanten sein. |

### setLocation(String value) {#setLocation-java.lang.String}
```
public void setLocation(String value)
```


Setzt den Ort der Signatur.

 **Remarks:** 

Der Standardwert ist  null .

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Ort der Signatur. |

### setReason(String value) {#setReason-java.lang.String}
```
public void setReason(String value)
```


Setzt den Grund der Signatur.

 **Remarks:** 

Der Standardwert ist  null .

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Grund für die Signatur. |

### setSignatureDate(Date value) {#setSignatureDate-java.util.Date}
```
public void setSignatureDate(Date value)
```


Setzt das Datum der Signatur.

 **Remarks:** 

Der Standardwert ist die aktuelle Zeit.

Dieser Wert wird in der digitalen Signatur als nicht verifizierte Computerzeit angezeigt.

 **Examples:** 

Zeigt, wie man ein erzeugtes PDF-Dokument signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.util.Date | Das Datum der Signatur. |

### setTimestampSettings(PdfDigitalSignatureTimestampSettings value) {#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings}
```
public void setTimestampSettings(PdfDigitalSignatureTimestampSettings value)
```


Setzt die Einstellungen für den Zeitstempel der digitalen Signatur.

 **Remarks:** 

Der Standardwert ist  null  und die digitale Signatur wird nicht mit einem Zeitstempel versehen. Wenn diese Eigenschaft auf ein gültiges [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) Objekt gesetzt wird, dann wird die digitale Signatur im PDF-Dokument mit einem Zeitstempel versehen.

 **Examples:** 

Zeigt, wie ein gespeichertes PDF-Dokument digital signiert und mit einem Zeitstempel versehen wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) | Die Einstellungen für den Zeitstempel der digitalen Signatur. |

