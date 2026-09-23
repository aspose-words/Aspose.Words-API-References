---
title: "DigitalSignatureDetails"
linktitle: "DigitalSignatureDetails"
second_title: "Aspose.Words for Java"
description: "包含在 Java 中使用数字签名对文档进行签名的详细信息。"
type: docs
weight: 152
url: /zh/java/com.aspose.words/digitalsignaturedetails/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignatureDetails
```

包含使用数字签名对文档进行签名的详细信息。

 **Examples:** 

展示如何签署 OOXML 文档。

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
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)](#DigitalSignatureDetails-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions) | 初始化一个新的 [DigitalSignatureDetails](../../com.aspose.words/digitalsignaturedetails/) 类实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | 获取一个包含用于签署文档的证书的 [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) 对象。 |
| [getSignOptions()](#getSignOptions) | 获取一个用于签署文档的 [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) 对象。 |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | 设置一个包含用于签署文档的证书的 [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) 对象。 |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | 设置一个用于签署文档的 [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) 对象。 |
### DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions) {#DigitalSignatureDetails-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions}
```
public DigitalSignatureDetails(CertificateHolder certificateHolder, SignOptions signOptions)
```


初始化一个新的 [DigitalSignatureDetails](../../com.aspose.words/digitalsignaturedetails/) 类实例。

 **Examples:** 

展示如何签署 OOXML 文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| certificateHolder | [CertificateHolder](../../com.aspose.words/certificateholder/) | 一个证书持有者，其中包含证书本身。 |
| signOptions | [SignOptions](../../com.aspose.words/signoptions/) | 用于签署文档的签名选项。 |

### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


获取一个包含用于签署文档的证书的 [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) 对象。

 **Examples:** 

展示如何签署 OOXML 文档。

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


获取一个用于签署文档的 [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) 对象。

 **Examples:** 

展示如何签署 OOXML 文档。

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


设置一个包含用于签署文档的证书的 [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) 对象。

 **Examples:** 

展示如何签署 OOXML 文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | 一个包含用于签署文档的证书的 [getCertificateHolder()](../../com.aspose.words/digitalsignaturedetails/\#getCertificateHolder) / [setCertificateHolder(com.aspose.words.CertificateHolder)](../../com.aspose.words/digitalsignaturedetails/\#setCertificateHolder-com.aspose.words.CertificateHolder) 对象。 |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


设置一个用于签署文档的 [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) 对象。

 **Examples:** 

展示如何签署 OOXML 文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | 一个用于签署文档的 [getSignOptions()](../../com.aspose.words/digitalsignaturedetails/\#getSignOptions) / [setSignOptions(com.aspose.words.SignOptions)](../../com.aspose.words/digitalsignaturedetails/\#setSignOptions-com.aspose.words.SignOptions) 对象。 |

