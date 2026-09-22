---
title: "DigitalSignatureDetails"
linktitle: "DigitalSignatureDetails"
second_title: "Aspose.Words لـ Java"
description: "يحتوي على تفاصيل لتوقيع مستند باستخدام توقيع رقمي في جافا."
type: docs
weight: 152
url: /ar/java/com.aspose.words/digitalsignaturedetails/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignatureDetails
```

يحتوي على تفاصيل لتوقيع مستند باستخدام توقيع رقمي.

 **Examples:** 

يوضح كيفية توقيع مستند OOXML.

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)](#DigitalSignatureDetails-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions) | ينشئ مثيلاً جديداً من الفئة [DigitalSignatureDetails](../../com.aspose.words/digitalsignaturedetails/). |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | يحصل على كائن [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) يحتوي على الشهادة المستخدمة لتوقيع مستند. |
| [getSignOptions()](#getSignOptions) | يحصل على كائن [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) يُستخدم لتوقيع مستند. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | يضبط كائن [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) يحتوي على الشهادة المستخدمة لتوقيع مستند. |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | يضبط كائن [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) يُستخدم لتوقيع مستند. |
### DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions) {#DigitalSignatureDetails-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions}
```
public DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)
```


ينشئ مثيلاً جديداً من الفئة [DigitalSignatureDetails](../../com.aspose.words/digitalsignaturedetails/).

 **Examples:** 

يوضح كيفية توقيع مستند OOXML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| certificateHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) | حامل شهادة يحتوي على الشهادة نفسها. |
| signOptions | [SignOptions](../../com.aspose.words/signoptions/) | خيارات التوقيع لاستخدامها في توقيع مستند. |

### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


يحصل على كائن [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) يحتوي على الشهادة المستخدمة لتوقيع مستند.

 **Examples:** 

يوضح كيفية توقيع مستند OOXML.

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


يحصل على كائن [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) يُستخدم لتوقيع مستند.

 **Examples:** 

يوضح كيفية توقيع مستند OOXML.

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


يضبط كائن [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) يحتوي على الشهادة المستخدمة لتوقيع مستند.

 **Examples:** 

يوضح كيفية توقيع مستند OOXML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | كائن [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) يحتوي على الشهادة المستخدمة لتوقيع مستند. |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


يضبط كائن [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) يُستخدم لتوقيع مستند.

 **Examples:** 

يوضح كيفية توقيع مستند OOXML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | كائن [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) يُستخدم لتوقيع مستند. |

