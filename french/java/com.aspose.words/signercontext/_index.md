---
title: "SignerContext"
linktitle: "SignerContext"
second_title: "Aspose.Words pour Java"
description: "Contexte du signataire de document en Java."
type: docs
weight: 623
url: /fr/java/com.aspose.words/signercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SignerContext extends ProcessorContext
```

Contexte du signataire du document
## Méthodes

| Méthode | Description |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | Objet CertificateHolder avec le certificat utilisé pour signer le fichier. |
| [getFontSettings()](#getFontSettings) | Paramètres de police utilisés par le processeur. |
| [getLayoutOptions()](#getLayoutOptions) | Options de mise en page du document utilisées par le processeur. |
| [getSignOptions()](#getSignOptions) | Objet SignOptions avec diverses options de signature. |
| [getWarningCallback()](#getWarningCallback) | Rappel d'avertissement utilisé par le processeur. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | Objet CertificateHolder avec le certificat utilisé pour signer le fichier. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Paramètres de police utilisés par le processeur. |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | Objet SignOptions avec diverses options de signature. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Rappel d'avertissement utilisé par le processeur. |
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Objet CertificateHolder avec le certificat utilisé pour signer le fichier.

 **Remarks:** 

Le certificat dans le détenteur DOIT contenir des clés privées et avoir le drapeau X509KeyStorageFlags.Exportable défini.

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The corresponding [CertificateHolder](../../com.aspose.words/certificateholder/) value.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Paramètres de police utilisés par le processeur.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Options de mise en page du document utilisées par le processeur.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getSignOptions() {#getSignOptions}
```
public SignOptions getSignOptions()
```


Objet SignOptions avec diverses options de signature.

**Returns:**
[SignOptions](../../com.aspose.words/signoptions/) - The corresponding [SignOptions](../../com.aspose.words/signoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Rappel d'avertissement utilisé par le processeur.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder}
```
public void setCertificateHolder(CertificateHolder value)
```


Objet CertificateHolder avec le certificat utilisé pour signer le fichier.

 **Remarks:** 

Le certificat dans le détenteur DOIT contenir des clés privées et avoir le drapeau X509KeyStorageFlags.Exportable défini.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | La valeur correspondante [CertificateHolder](../../com.aspose.words/certificateholder/). |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Paramètres de police utilisés par le processeur.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | La valeur correspondante de [FontSettings](../../com.aspose.words/fontsettings/). |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


Objet SignOptions avec diverses options de signature.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | La valeur correspondante [SignOptions](../../com.aspose.words/signoptions/). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Rappel d'avertissement utilisé par le processeur.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | La valeur correspondante de [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

