---
title: "SignerContext"
linktitle: "SignerContext"
second_title: "Aspose.Words für Java"
description: "Signer‑Kontext für Dokumente in Java."
type: docs
weight: 623
url: /de/java/com.aspose.words/signercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SignerContext extends ProcessorContext
```

Kontext des Dokumentenunterzeichners
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | CertificateHolder‑Objekt mit dem Zertifikat, das zum Signieren der Datei verwendet wird. |
| [getFontSettings()](#getFontSettings) | Schrifteinstellungen, die vom Prozessor verwendet werden. |
| [getLayoutOptions()](#getLayoutOptions) | Dokumentenlayout‑Optionen, die vom Prozessor verwendet werden. |
| [getSignOptions()](#getSignOptions) | SignOptions‑Objekt mit verschiedenen Signieroptionen. |
| [getWarningCallback()](#getWarningCallback) | Warn‑Callback, das vom Prozessor verwendet wird. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | CertificateHolder‑Objekt mit dem Zertifikat, das zum Signieren der Datei verwendet wird. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Schrifteinstellungen, die vom Prozessor verwendet werden. |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | SignOptions‑Objekt mit verschiedenen Signieroptionen. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Warn‑Callback, das vom Prozessor verwendet wird. |
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


CertificateHolder‑Objekt mit dem Zertifikat, das zum Signieren der Datei verwendet wird.

 **Remarks:** 

Das Zertifikat im Holder MUSS private Schlüssel enthalten und das Flag X509KeyStorageFlags.Exportable gesetzt sein.

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The corresponding [CertificateHolder](../../com.aspose.words/certificateholder/) value.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Schrifteinstellungen, die vom Prozessor verwendet werden.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Dokumentenlayout‑Optionen, die vom Prozessor verwendet werden.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getSignOptions() {#getSignOptions}
```
public SignOptions getSignOptions()
```


SignOptions‑Objekt mit verschiedenen Signieroptionen.

**Returns:**
[SignOptions](../../com.aspose.words/signoptions/) - The corresponding [SignOptions](../../com.aspose.words/signoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Warn‑Callback, das vom Prozessor verwendet wird.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder}
```
public void setCertificateHolder(CertificateHolder value)
```


CertificateHolder‑Objekt mit dem Zertifikat, das zum Signieren der Datei verwendet wird.

 **Remarks:** 

Das Zertifikat im Holder MUSS private Schlüssel enthalten und das Flag X509KeyStorageFlags.Exportable gesetzt sein.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | Der entsprechende [CertificateHolder](../../com.aspose.words/certificateholder/)‑Wert. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Schrifteinstellungen, die vom Prozessor verwendet werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | Der entsprechende [FontSettings](../../com.aspose.words/fontsettings/) Wert. |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


SignOptions‑Objekt mit verschiedenen Signieroptionen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | Der entsprechende [SignOptions](../../com.aspose.words/signoptions/)‑Wert. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Warn‑Callback, das vom Prozessor verwendet wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Der entsprechende [IWarningCallback](../../com.aspose.words/iwarningcallback/) Wert. |

