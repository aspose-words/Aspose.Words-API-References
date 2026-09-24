---
title: "SignerContext"
linktitle: "SignerContext"
second_title: "Aspose.Words para Java"
description: "Contexto del firmante del documento en Java."
type: docs
weight: 623
url: /es/java/com.aspose.words/signercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SignerContext extends ProcessorContext
```

Contexto del firmante del documento
## Métodos

| Método | Descripción |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | Objeto CertificateHolder con el certificado que se utilizó para firmar el archivo. |
| [getFontSettings()](#getFontSettings) | Configuración de fuentes utilizada por el procesador. |
| [getLayoutOptions()](#getLayoutOptions) | Opciones de diseño del documento utilizadas por el procesador. |
| [getSignOptions()](#getSignOptions) | Objeto SignOptions con varias opciones de firma. |
| [getWarningCallback()](#getWarningCallback) | Callback de advertencia utilizado por el procesador. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | Objeto CertificateHolder con el certificado que se utilizó para firmar el archivo. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Configuración de fuentes utilizada por el procesador. |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | Objeto SignOptions con varias opciones de firma. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Callback de advertencia utilizado por el procesador. |
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Objeto CertificateHolder con el certificado que se utilizó para firmar el archivo.

 **Remarks:** 

El certificado en el contenedor DEBE contener claves privadas y tener la bandera X509KeyStorageFlags.Exportable establecida.

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The corresponding [CertificateHolder](../../com.aspose.words/certificateholder/) value.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Configuración de fuentes utilizada por el procesador.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Opciones de diseño del documento utilizadas por el procesador.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getSignOptions() {#getSignOptions}
```
public SignOptions getSignOptions()
```


Objeto SignOptions con varias opciones de firma.

**Returns:**
[SignOptions](../../com.aspose.words/signoptions/) - The corresponding [SignOptions](../../com.aspose.words/signoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Callback de advertencia utilizado por el procesador.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder}
```
public void setCertificateHolder(CertificateHolder value)
```


Objeto CertificateHolder con el certificado que se utilizó para firmar el archivo.

 **Remarks:** 

El certificado en el contenedor DEBE contener claves privadas y tener la bandera X509KeyStorageFlags.Exportable establecida.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | El valor correspondiente de [CertificateHolder](../../com.aspose.words/certificateholder/). |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Configuración de fuentes utilizada por el procesador.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | El valor correspondiente de [FontSettings](../../com.aspose.words/fontsettings/). |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


Objeto SignOptions con varias opciones de firma.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | El valor correspondiente de [SignOptions](../../com.aspose.words/signoptions/). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Callback de advertencia utilizado por el procesador.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | El valor correspondiente de [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

