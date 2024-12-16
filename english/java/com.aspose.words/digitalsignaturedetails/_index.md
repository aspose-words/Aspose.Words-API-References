---
title: DigitalSignatureDetails
linktitle: DigitalSignatureDetails
second_title: Aspose.Words for Java
description: Contains details for signing a document with a digital signature in Java.
type: docs
weight: 147
url: /java/com.aspose.words/digitalsignaturedetails/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignatureDetails
```

Contains details for signing a document with a digital signature.

 **Examples:** 

Shows how to sign OOXML document.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)](#DigitalSignatureDetails-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions) | Initializes a new instance of [DigitalSignatureDetails](../../com.aspose.words/digitalsignaturedetails/) class. |
## Methods

| Method | Description |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | Gets a [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) object that contains the certificate used to sign a document. |
| [getSignOptions()](#getSignOptions) | Gets a [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) object used to sign a document. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | Sets a [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) object that contains the certificate used to sign a document. |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | Sets a [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) object used to sign a document. |
### DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions) {#DigitalSignatureDetails-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions}
```
public DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)
```


Initializes a new instance of [DigitalSignatureDetails](../../com.aspose.words/digitalsignaturedetails/) class.

 **Examples:** 

Shows how to sign OOXML document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| certificateHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) | A certificate holder which contains the certificate itself. |
| signOptions | [SignOptions](../../com.aspose.words/signoptions/) | Signature options to use for signing a document. |

### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Gets a [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) object that contains the certificate used to sign a document.

 **Examples:** 

Shows how to sign OOXML document.

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


Gets a [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) object used to sign a document.

 **Examples:** 

Shows how to sign OOXML document.

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


Sets a [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) object that contains the certificate used to sign a document.

 **Examples:** 

Shows how to sign OOXML document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | A [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) object that contains the certificate used to sign a document. |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


Sets a [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) object used to sign a document.

 **Examples:** 

Shows how to sign OOXML document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | A [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) object used to sign a document. |

