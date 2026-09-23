---
title: "DigitalSignatureDetails"
linktitle: "DigitalSignatureDetails"
second_title: "Aspose.Words für Java"
description: "Enthält Details zum Signieren eines Dokuments mit einer digitalen Signatur in Java."
type: docs
weight: 152
url: /de/java/com.aspose.words/digitalsignaturedetails/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignatureDetails
```

Enthält Details zum Signieren eines Dokuments mit einer digitalen Signatur.

 **Examples:** 

Zeigt, wie man ein OOXML-Dokument signiert.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 SignOptions signOptions = new SignOptions();
 signOptions.setComments("Some comments");
 signOptions.setSignTime(new Date());
 saveOptions.setDigitalSignatureDetails(new DigitalSignatureDetails(
         certificateHolder,
         signOptions));

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
 
```
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)](#DigitalSignatureDetails-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions) | Initialisiert eine neue Instanz der Klasse [DigitalSignatureDetails](../../com.aspose.words/digitalsignaturedetails/). |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | Ruft ein [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) Objekt ab, das das zum Signieren eines Dokuments verwendete Zertifikat enthält. |
| [getSignOptions()](#getSignOptions) | Ruft ein [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) Objekt ab, das zum Signieren eines Dokuments verwendet wird. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | Legt ein [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) Objekt fest, das das zum Signieren eines Dokuments verwendete Zertifikat enthält. |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | Legt ein [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) Objekt fest, das zum Signieren eines Dokuments verwendet wird. |
### DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions) {#DigitalSignatureDetails-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions}
```
public DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)
```


Initialisiert eine neue Instanz der Klasse [DigitalSignatureDetails](../../com.aspose.words/digitalsignaturedetails/).

 **Examples:** 

Zeigt, wie man ein OOXML-Dokument signiert.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 SignOptions signOptions = new SignOptions();
 signOptions.setComments("Some comments");
 signOptions.setSignTime(new Date());
 saveOptions.setDigitalSignatureDetails(new DigitalSignatureDetails(
         certificateHolder,
         signOptions));

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| certificateHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) | Ein Zertifikatsinhaber, der das Zertifikat selbst enthält. |
| signOptions | [SignOptions](../../com.aspose.words/signoptions/) | Signaturoptionen, die zum Signieren eines Dokuments verwendet werden. |

### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Ruft ein [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) Objekt ab, das das zum Signieren eines Dokuments verwendete Zertifikat enthält.

 **Examples:** 

Zeigt, wie man ein OOXML-Dokument signiert.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 SignOptions signOptions = new SignOptions();
 signOptions.setComments("Some comments");
 signOptions.setSignTime(new Date());
 saveOptions.setDigitalSignatureDetails(new DigitalSignatureDetails(
         certificateHolder,
         signOptions));

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
 
```

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - A [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) object that contains the certificate used to sign a document.
### getSignOptions() {#getSignOptions}
```
public SignOptions getSignOptions()
```


Ruft ein [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) Objekt ab, das zum Signieren eines Dokuments verwendet wird.

 **Examples:** 

Zeigt, wie man ein OOXML-Dokument signiert.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 SignOptions signOptions = new SignOptions();
 signOptions.setComments("Some comments");
 signOptions.setSignTime(new Date());
 saveOptions.setDigitalSignatureDetails(new DigitalSignatureDetails(
         certificateHolder,
         signOptions));

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
 
```

**Returns:**
[SignOptions](../../com.aspose.words/signoptions/) - A [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) object used to sign a document.
### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder}
```
public void setCertificateHolder(CertificateHolder value)
```


Legt ein [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) Objekt fest, das das zum Signieren eines Dokuments verwendete Zertifikat enthält.

 **Examples:** 

Zeigt, wie man ein OOXML-Dokument signiert.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 SignOptions signOptions = new SignOptions();
 signOptions.setComments("Some comments");
 signOptions.setSignTime(new Date());
 saveOptions.setDigitalSignatureDetails(new DigitalSignatureDetails(
         certificateHolder,
         signOptions));

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | Ein [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) Objekt, das das zum Signieren eines Dokuments verwendete Zertifikat enthält. |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


Legt ein [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) Objekt fest, das zum Signieren eines Dokuments verwendet wird.

 **Examples:** 

Zeigt, wie man ein OOXML-Dokument signiert.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 SignOptions signOptions = new SignOptions();
 signOptions.setComments("Some comments");
 signOptions.setSignTime(new Date());
 saveOptions.setDigitalSignatureDetails(new DigitalSignatureDetails(
         certificateHolder,
         signOptions));

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.DigitalSignature.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | Ein [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) Objekt, das zum Signieren eines Dokuments verwendet wird. |

