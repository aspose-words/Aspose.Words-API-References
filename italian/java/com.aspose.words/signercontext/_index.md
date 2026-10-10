---
title: "SignerContext"
linktitle: "SignerContext"
second_title: "Aspose.Words per Java"
description: "Contesto del firmatario del documento in Java."
type: docs
weight: 623
url: /it/java/com.aspose.words/signercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SignerContext extends ProcessorContext
```

Contesto del firmatario del documento.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | Oggetto CertificateHolder con certificato utilizzato per firmare il file. |
| [getFontSettings()](#getFontSettings) | Impostazioni dei caratteri utilizzate dal processore. |
| [getLayoutOptions()](#getLayoutOptions) | Opzioni di layout del documento utilizzate dal processore. |
| [getSignOptions()](#getSignOptions) | Oggetto SignOptions con varie opzioni di firma. |
| [getWarningCallback()](#getWarningCallback) | Callback di avviso utilizzato dal processore. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | Oggetto CertificateHolder con certificato utilizzato per firmare il file. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Impostazioni dei caratteri utilizzate dal processore. |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | Oggetto SignOptions con varie opzioni di firma. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Callback di avviso utilizzato dal processore. |
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Oggetto CertificateHolder con certificato utilizzato per firmare il file.

 **Remarks:** 

Il certificato nel contenitore DEVE contenere chiavi private e avere impostata la flag X509KeyStorageFlags.Exportable.

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The corresponding [CertificateHolder](../../com.aspose.words/certificateholder/) value.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Impostazioni dei caratteri utilizzate dal processore.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Opzioni di layout del documento utilizzate dal processore.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getSignOptions() {#getSignOptions}
```
public SignOptions getSignOptions()
```


Oggetto SignOptions con varie opzioni di firma.

**Returns:**
[SignOptions](../../com.aspose.words/signoptions/) - The corresponding [SignOptions](../../com.aspose.words/signoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Callback di avviso utilizzato dal processore.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder}
```
public void setCertificateHolder(CertificateHolder value)
```


Oggetto CertificateHolder con certificato utilizzato per firmare il file.

 **Remarks:** 

Il certificato nel contenitore DEVE contenere chiavi private e avere impostata la flag X509KeyStorageFlags.Exportable.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | Il valore corrispondente di [CertificateHolder](../../com.aspose.words/certificateholder/). |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Impostazioni dei caratteri utilizzate dal processore.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | Il valore corrispondente di [FontSettings](../../com.aspose.words/fontsettings/). |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


Oggetto SignOptions con varie opzioni di firma.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | Il valore corrispondente di [SignOptions](../../com.aspose.words/signoptions/). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Callback di avviso utilizzato dal processore.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Il valore corrispondente di [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

