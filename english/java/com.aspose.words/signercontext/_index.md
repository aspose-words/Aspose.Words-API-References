---
title: SignerContext
linktitle: SignerContext
second_title: Aspose.Words for Java
description: Document signer context in Java.
type: docs
weight: 620
url: /java/com.aspose.words/signercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SignerContext extends ProcessorContext
```

Document signer context
## Methods

| Method | Description |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | CertificateHolder object with certificate that used to sign file. |
| [getFontSettings()](#getFontSettings) | Font settings used by the processor. |
| [getLayoutOptions()](#getLayoutOptions) | Document layout options used by the processor. |
| [getSignOptions()](#getSignOptions) | SignOptions object with various signing options. |
| [getWarningCallback()](#getWarningCallback) | Warning callback used by the processor. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | CertificateHolder object with certificate that used to sign file. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Font settings used by the processor. |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | SignOptions object with various signing options. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Warning callback used by the processor. |
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


CertificateHolder object with certificate that used to sign file.

 **Remarks:** 

The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set.

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The corresponding [CertificateHolder](../../com.aspose.words/certificateholder/) value.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Font settings used by the processor.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Document layout options used by the processor.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getSignOptions() {#getSignOptions}
```
public SignOptions getSignOptions()
```


SignOptions object with various signing options.

**Returns:**
[SignOptions](../../com.aspose.words/signoptions/) - The corresponding [SignOptions](../../com.aspose.words/signoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Warning callback used by the processor.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder}
```
public void setCertificateHolder(CertificateHolder value)
```


CertificateHolder object with certificate that used to sign file.

 **Remarks:** 

The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | The corresponding [CertificateHolder](../../com.aspose.words/certificateholder/) value. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Font settings used by the processor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value. |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


SignOptions object with various signing options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | The corresponding [SignOptions](../../com.aspose.words/signoptions/) value. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Warning callback used by the processor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value. |

