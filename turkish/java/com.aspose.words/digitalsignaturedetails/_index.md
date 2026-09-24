---
title: "DigitalSignatureDetails"
linktitle: "DigitalSignatureDetails"
second_title: "Aspose.Words Java için"
description: "Java'da bir belgeyi dijital imza ile imzalamak için ayrıntıları içerir."
type: docs
weight: 152
url: /tr/java/com.aspose.words/digitalsignaturedetails/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignatureDetails
```

Bir belgeyi dijital imza ile imzalamak için ayrıntıları içerir.

 **Examples:** 

OOXML belgesinin nasıl imzalanacağını gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)](#DigitalSignatureDetails-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions) | [DigitalSignatureDetails](../../com.aspose.words/digitalsignaturedetails/) sınıfının yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | Belgeyi imzalamak için kullanılan sertifikayı içeren bir [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) nesnesini alır. |
| [getSignOptions()](#getSignOptions) | Belgeyi imzalamak için kullanılan bir [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) nesnesini alır. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | Belgeyi imzalamak için kullanılan sertifikayı içeren bir [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) nesnesini ayarlar. |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | Belgeyi imzalamak için kullanılan bir [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) nesnesini ayarlar. |
### DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions) {#DigitalSignatureDetails-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions}
```
public DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)
```


[DigitalSignatureDetails](../../com.aspose.words/digitalsignaturedetails/) sınıfının yeni bir örneğini başlatır.

 **Examples:** 

OOXML belgesinin nasıl imzalanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| certificateHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) | Sertifikayı kendisi içinde barındıran bir sertifika tutucu. |
| signOptions | [SignOptions](../../com.aspose.words/signoptions/) | Bir belgeyi imzalamak için kullanılacak imza seçenekleri. |

### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Belgeyi imzalamak için kullanılan sertifikayı içeren bir [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) nesnesini alır.

 **Examples:** 

OOXML belgesinin nasıl imzalanacağını gösterir.

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


Belgeyi imzalamak için kullanılan bir [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) nesnesini alır.

 **Examples:** 

OOXML belgesinin nasıl imzalanacağını gösterir.

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


Belgeyi imzalamak için kullanılan sertifikayı içeren bir [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) nesnesini ayarlar.

 **Examples:** 

OOXML belgesinin nasıl imzalanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | Belgeyi imzalamak için kullanılan sertifikayı içeren bir [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) nesnesi. |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


Belgeyi imzalamak için kullanılan bir [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) nesnesini ayarlar.

 **Examples:** 

OOXML belgesinin nasıl imzalanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | Belgeyi imzalamak için kullanılan bir [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) nesnesi. |

