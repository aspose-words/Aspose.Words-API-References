---
title: "SignerContext"
linktitle: "SignerContext"
second_title: "Aspose.Words for Java"
description: "Java 中的文档签名上下文。"
type: docs
weight: 623
url: /zh/java/com.aspose.words/signercontext/
---

**Inheritance:**
java.lang.Object，[com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SignerContext extends ProcessorContext
```

文档签名上下文
## 方法

| 方法 | 描述 |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | 包含用于签署文件的证书的 CertificateHolder 对象。 |
| [getFontSettings()](#getFontSettings) | 处理器使用的字体设置。 |
| [getLayoutOptions()](#getLayoutOptions) | 处理器使用的文档布局选项。 |
| [getSignOptions()](#getSignOptions) | 具有各种签名选项的 SignOptions 对象。 |
| [getWarningCallback()](#getWarningCallback) | 处理器使用的警告回调。 |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | 包含用于签署文件的证书的 CertificateHolder 对象。 |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | 处理器使用的字体设置。 |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | 具有各种签名选项的 SignOptions 对象。 |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | 处理器使用的警告回调。 |
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


包含用于签署文件的证书的 CertificateHolder 对象。

 **Remarks:** 

持有者中的证书必须包含私钥，并且设置了 X509KeyStorageFlags.Exportable 标志。

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The corresponding [CertificateHolder](../../com.aspose.words/certificateholder/) value.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


处理器使用的字体设置。

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


处理器使用的文档布局选项。

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getSignOptions() {#getSignOptions}
```
public SignOptions getSignOptions()
```


具有各种签名选项的 SignOptions 对象。

**Returns:**
[SignOptions](../../com.aspose.words/signoptions/) - The corresponding [SignOptions](../../com.aspose.words/signoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


处理器使用的警告回调。

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder}
```
public void setCertificateHolder(CertificateHolder value)
```


包含用于签署文件的证书的 CertificateHolder 对象。

 **Remarks:** 

持有者中的证书必须包含私钥，并且设置了 X509KeyStorageFlags.Exportable 标志。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | 对应的 [CertificateHolder](../../com.aspose.words/certificateholder/) 值。 |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


处理器使用的字体设置。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | 对应的[FontSettings](../../com.aspose.words/fontsettings/)值。 |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


具有各种签名选项的 SignOptions 对象。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | 对应的 [SignOptions](../../com.aspose.words/signoptions/) 值。 |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


处理器使用的警告回调。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | 对应的[IWarningCallback](../../com.aspose.words/iwarningcallback/)值。 |

