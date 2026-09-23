---
title: "PdfDigitalSignatureDetails"
linktitle: "PdfDigitalSignatureDetails"
second_title: "Aspose.Words per Java"
description: "Contiene i dettagli per firmare un documento PDF con una firma digitale in Java."
type: docs
weight: 531
url: /it/java/com.aspose.words/pdfdigitalsignaturedetails/
---

**Inheritance:**
java.lang.Object
```
public class PdfDigitalSignatureDetails
```

Contiene i dettagli per firmare un documento PDF con una firma digitale.

 **Remarks:** 

Al momento la firma digitale dei documenti PDF è disponibile solo su .NET 3.5 o versioni successive.

Per firmare digitalmente un documento PDF quando viene creato da Aspose.Words, impostare la proprietà [PdfSaveOptions.getDigitalSignatureDetails()](../../com.aspose.words/pdfsaveoptions/\#getDigitalSignatureDetails) / [PdfSaveOptions.setDigitalSignatureDetails(com.aspose.words.PdfDigitalSignatureDetails)](../../com.aspose.words/pdfsaveoptions/\#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails) su un oggetto valido [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails/) e quindi salvare il documento nel formato PDF passando i [PdfSaveOptions](../../com.aspose.words/pdfsaveoptions/) come parametro al metodo [Document.save(java.lang.String, com.aspose.words.SaveOptions)](../../com.aspose.words/document/\#save-java.lang.String--com.aspose.words.SaveOptions).

Aspose.Words crea una firma PKCS\#7 sull'intero documento PDF e utilizza il filtro "Adobe.PPKMS" e il sottofiltro "adbe.pkcs7.sha1" durante la creazione di una firma digitale.

 **Examples:** 

Mostra come firmare un documento PDF generato.

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
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [PdfDigitalSignatureDetails()](#PdfDigitalSignatureDetails) | Inizializza un'istanza di questa classe. |
| [PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate)](#PdfDigitalSignatureDetails-com.aspose.words.CertificateHolder-java.lang.String-java.lang.String-java.util.Date) | Inizializza un'istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | Restituisce l'oggetto titolare del certificato che contiene il certificato usato per firmare il documento. |
| [getHashAlgorithm()](#getHashAlgorithm) | Ottiene l'algoritmo hash. |
| [getLocation()](#getLocation) | Ottiene la posizione della firma. |
| [getReason()](#getReason) | Ottiene il motivo della firma. |
| [getSignatureDate()](#getSignatureDate) | Ottiene la data della firma. |
| [getTimestampSettings()](#getTimestampSettings) | Ottiene le impostazioni del timestamp della firma digitale. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | Restituisce l'oggetto titolare del certificato che contiene il certificato usato per firmare il documento. |
| [setHashAlgorithm(int value)](#setHashAlgorithm-int) | Imposta l'algoritmo hash. |
| [setLocation(String value)](#setLocation-java.lang.String) | Imposta la posizione della firma. |
| [setReason(String value)](#setReason-java.lang.String) | Imposta il motivo della firma. |
| [setSignatureDate(Date value)](#setSignatureDate-java.util.Date) | Imposta la data della firma. |
| [setTimestampSettings(PdfDigitalSignatureTimestampSettings value)](#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings) | Imposta le impostazioni del timestamp della firma digitale. |
### PdfDigitalSignatureDetails() {#PdfDigitalSignatureDetails}
```
public PdfDigitalSignatureDetails()
```


Inizializza un'istanza di questa classe.

 **Examples:** 

Mostra come firmare un documento PDF generato.

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


Inizializza un'istanza di questa classe.

 **Examples:** 

Mostra come firmare un documento PDF generato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| certificateHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) | Un contenitore di certificati che contiene il certificato stesso. |
| motivo | java.lang.String | Il motivo della firma. |
| posizione | java.lang.String | Il luogo della firma. |
| signatureDate | java.util.Date | Data e ora della firma. |

### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Restituisce l'oggetto titolare del certificato che contiene il certificato usato per firmare il documento.

 **Examples:** 

Mostra come firmare un documento PDF generato.

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


Ottiene l'algoritmo hash.

 **Remarks:** 

Il valore predefinito è l'algoritmo SHA-256.

 **Examples:** 

Mostra come firmare un documento PDF generato.

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
int - L'algoritmo di hash. Il valore restituito è una delle costanti [PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm/).
### getLocation() {#getLocation}
```
public String getLocation()
```


Ottiene la posizione della firma.

 **Remarks:** 

Il valore predefinito è  null .

 **Examples:** 

Mostra come firmare un documento PDF generato.

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
java.lang.String - Il luogo della firma.
### getReason() {#getReason}
```
public String getReason()
```


Ottiene il motivo della firma.

 **Remarks:** 

Il valore predefinito è  null .

 **Examples:** 

Mostra come firmare un documento PDF generato.

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
java.lang.String - Il motivo della firma.
### getSignatureDate() {#getSignatureDate}
```
public Date getSignatureDate()
```


Ottiene la data della firma.

 **Remarks:** 

Il valore predefinito è l'ora corrente.

Questo valore apparirà nella firma digitale come un'ora del computer non verificata.

 **Examples:** 

Mostra come firmare un documento PDF generato.

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
java.util.Date - La data della firma.
### getTimestampSettings() {#getTimestampSettings}
```
public PdfDigitalSignatureTimestampSettings getTimestampSettings()
```


Ottiene le impostazioni del timestamp della firma digitale.

 **Remarks:** 

Il valore predefinito è  null  e la firma digitale non sarà timbrata. Quando questa proprietà è impostata su un oggetto valido [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/), la firma digitale nel documento PDF sarà timbrata.

 **Examples:** 

Mostra come firmare digitalmente un documento PDF salvato e aggiungere il timestamp.

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


Restituisce l'oggetto titolare del certificato che contiene il certificato usato per firmare il documento.

 **Examples:** 

Mostra come firmare un documento PDF generato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | L'oggetto titolare del certificato che contiene il certificato è stato usato per firmare il documento. |

### setHashAlgorithm(int value) {#setHashAlgorithm-int}
```
public void setHashAlgorithm(int value)
```


Imposta l'algoritmo hash.

 **Remarks:** 

Il valore predefinito è l'algoritmo SHA-256.

 **Examples:** 

Mostra come firmare un documento PDF generato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | L'algoritmo di hash. Il valore deve essere una delle costanti [PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm/). |

### setLocation(String value) {#setLocation-java.lang.String}
```
public void setLocation(String value)
```


Imposta la posizione della firma.

 **Remarks:** 

Il valore predefinito è  null .

 **Examples:** 

Mostra come firmare un documento PDF generato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il luogo della firma. |

### setReason(String value) {#setReason-java.lang.String}
```
public void setReason(String value)
```


Imposta il motivo della firma.

 **Remarks:** 

Il valore predefinito è  null .

 **Examples:** 

Mostra come firmare un documento PDF generato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il motivo della firma. |

### setSignatureDate(Date value) {#setSignatureDate-java.util.Date}
```
public void setSignatureDate(Date value)
```


Imposta la data della firma.

 **Remarks:** 

Il valore predefinito è l'ora corrente.

Questo valore apparirà nella firma digitale come un'ora del computer non verificata.

 **Examples:** 

Mostra come firmare un documento PDF generato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.util.Date | La data della firma. |

### setTimestampSettings(PdfDigitalSignatureTimestampSettings value) {#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings}
```
public void setTimestampSettings(PdfDigitalSignatureTimestampSettings value)
```


Imposta le impostazioni del timestamp della firma digitale.

 **Remarks:** 

Il valore predefinito è  null  e la firma digitale non sarà timbrata. Quando questa proprietà è impostata su un oggetto valido [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/), la firma digitale nel documento PDF sarà timbrata.

 **Examples:** 

Mostra come firmare digitalmente un documento PDF salvato e aggiungere il timestamp.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings/) | Le impostazioni del timestamp della firma digitale. |

