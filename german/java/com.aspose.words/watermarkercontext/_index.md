---
title: "WatermarkerContext"
linktitle: "WatermarkerContext"
second_title: "Aspose.Words für Java"
description: "Dokument-Watermarker-Kontext in Java."
type: docs
weight: 725
url: /de/java/com.aspose.words/watermarkercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class WatermarkerContext extends ProcessorContext
```

Dokument-Wasserzeichner-Kontext.

 **Examples:** 

Zeigt, wie man Wasserzeichentext in das Dokument einfügt, indem man den Kontext verwendet.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setTextWatermark(watermarkText);

 watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextText.docx")
         .execute();
 
```

Zeigt, wie man Wasserzeichentext aus einem Stream in das Dokument einfügt, indem man den Kontext verwendet.

```

 String watermarkText = "This is a watermark";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setTextWatermark(watermarkText);

     watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextTextStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

Zeigt, wie man ein Wasserzeichenbild in das Dokument einfügt, indem man den Kontext verwendet.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

 watermarkerContext.getImageWatermarkOptions().setScale(50.0);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextImage.docx")
         .execute();
 
```

Zeigt, wie man ein Wasserzeichenbild aus einem Stream in das Dokument einfügt, indem man den Kontext verwendet.

```

 String watermarkImage = getImageDir() + "Logo.jpg";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

     watermarkerContext.getImageWatermarkOptions().setScale(50.0);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextImageStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [WatermarkerContext()](#WatermarkerContext) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getFontSettings()](#getFontSettings) | Schrifteinstellungen, die vom Prozessor verwendet werden. |
| [getImageWatermark()](#getImageWatermark) | Bildbytes, die als Wasserzeichen verwendet werden sollen. |
| [getImageWatermarkOptions()](#getImageWatermarkOptions) | Optionen für das Textwasserzeichen. |
| [getLayoutOptions()](#getLayoutOptions) | Dokumentenlayout‑Optionen, die vom Prozessor verwendet werden. |
| [getTextWatermark()](#getTextWatermark) | Text, der als Wasserzeichen verwendet werden soll. |
| [getTextWatermarkOptions()](#getTextWatermarkOptions) | Optionen für das Bildwasserzeichen. |
| [getWarningCallback()](#getWarningCallback) | Warn‑Callback, das vom Prozessor verwendet wird. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Schrifteinstellungen, die vom Prozessor verwendet werden. |
| [setImageWatermark(byte[] value)](#setImageWatermark-byte) | Bildbytes, die als Wasserzeichen verwendet werden sollen. |
| [setTextWatermark(String value)](#setTextWatermark-java.lang.String) | Text, der als Wasserzeichen verwendet werden soll. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Warn‑Callback, das vom Prozessor verwendet wird. |
### WatermarkerContext() {#WatermarkerContext}
```
public WatermarkerContext()
```


Initialisiert eine neue Instanz dieser Klasse.

### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Schrifteinstellungen, die vom Prozessor verwendet werden.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getImageWatermark() {#getImageWatermark}
```
public byte[] getImageWatermark()
```


Bildbytes, die als Wasserzeichen verwendet werden sollen.

 **Remarks:** 

Wenn sowohl [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) als auch [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) angegeben sind, überschreibt das Textwasserzeichen das Bildwasserzeichen.

 **Examples:** 

Zeigt, wie man ein Wasserzeichenbild in das Dokument einfügt, indem man den Kontext verwendet.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

 watermarkerContext.getImageWatermarkOptions().setScale(50.0);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextImage.docx")
         .execute();
 
```

Zeigt, wie man ein Wasserzeichenbild aus einem Stream in das Dokument einfügt, indem man den Kontext verwendet.

```

 String watermarkImage = getImageDir() + "Logo.jpg";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

     watermarkerContext.getImageWatermarkOptions().setScale(50.0);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextImageStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
byte[] - Der entsprechende byte[]-Wert.
### getImageWatermarkOptions() {#getImageWatermarkOptions}
```
public ImageWatermarkOptions getImageWatermarkOptions()
```


Optionen für das Textwasserzeichen.

 **Examples:** 

Zeigt, wie man ein Wasserzeichenbild in das Dokument einfügt, indem man den Kontext verwendet.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

 watermarkerContext.getImageWatermarkOptions().setScale(50.0);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextImage.docx")
         .execute();
 
```

Zeigt, wie man ein Wasserzeichenbild aus einem Stream in das Dokument einfügt, indem man den Kontext verwendet.

```

 String watermarkImage = getImageDir() + "Logo.jpg";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

     watermarkerContext.getImageWatermarkOptions().setScale(50.0);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextImageStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
[ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) - The corresponding [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Dokumentenlayout‑Optionen, die vom Prozessor verwendet werden.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getTextWatermark() {#getTextWatermark}
```
public String getTextWatermark()
```


Text, der als Wasserzeichen verwendet werden soll.

 **Remarks:** 

Wenn sowohl [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) als auch [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) angegeben sind, überschreibt das Textwasserzeichen das Bildwasserzeichen.

 **Examples:** 

Zeigt, wie man Wasserzeichentext in das Dokument einfügt, indem man den Kontext verwendet.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setTextWatermark(watermarkText);

 watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextText.docx")
         .execute();
 
```

Zeigt, wie man Wasserzeichentext aus einem Stream in das Dokument einfügt, indem man den Kontext verwendet.

```

 String watermarkText = "This is a watermark";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setTextWatermark(watermarkText);

     watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextTextStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getTextWatermarkOptions() {#getTextWatermarkOptions}
```
public TextWatermarkOptions getTextWatermarkOptions()
```


Optionen für das Bildwasserzeichen.

 **Examples:** 

Zeigt, wie man Wasserzeichentext in das Dokument einfügt, indem man den Kontext verwendet.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setTextWatermark(watermarkText);

 watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextText.docx")
         .execute();
 
```

Zeigt, wie man Wasserzeichentext aus einem Stream in das Dokument einfügt, indem man den Kontext verwendet.

```

 String watermarkText = "This is a watermark";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setTextWatermark(watermarkText);

     watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextTextStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
[TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) - The corresponding [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Warn‑Callback, das vom Prozessor verwendet wird.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Schrifteinstellungen, die vom Prozessor verwendet werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | Der entsprechende [FontSettings](../../com.aspose.words/fontsettings/) Wert. |

### setImageWatermark(byte[] value) {#setImageWatermark-byte}
```
public void setImageWatermark(byte[] value)
```


Bildbytes, die als Wasserzeichen verwendet werden sollen.

 **Remarks:** 

Wenn sowohl [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) als auch [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) angegeben sind, überschreibt das Textwasserzeichen das Bildwasserzeichen.

 **Examples:** 

Zeigt, wie man ein Wasserzeichenbild in das Dokument einfügt, indem man den Kontext verwendet.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

 watermarkerContext.getImageWatermarkOptions().setScale(50.0);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextImage.docx")
         .execute();
 
```

Zeigt, wie man ein Wasserzeichenbild aus einem Stream in das Dokument einfügt, indem man den Kontext verwendet.

```

 String watermarkImage = getImageDir() + "Logo.jpg";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

     watermarkerContext.getImageWatermarkOptions().setScale(50.0);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextImageStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | byte[] | Der entsprechende byte[]-Wert. |

### setTextWatermark(String value) {#setTextWatermark-java.lang.String}
```
public void setTextWatermark(String value)
```


Text, der als Wasserzeichen verwendet werden soll.

 **Remarks:** 

Wenn sowohl [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) als auch [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) angegeben sind, überschreibt das Textwasserzeichen das Bildwasserzeichen.

 **Examples:** 

Zeigt, wie man Wasserzeichentext in das Dokument einfügt, indem man den Kontext verwendet.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setTextWatermark(watermarkText);

 watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextText.docx")
         .execute();
 
```

Zeigt, wie man Wasserzeichentext aus einem Stream in das Dokument einfügt, indem man den Kontext verwendet.

```

 String watermarkText = "This is a watermark";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setTextWatermark(watermarkText);

     watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextTextStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Warn‑Callback, das vom Prozessor verwendet wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Der entsprechende [IWarningCallback](../../com.aspose.words/iwarningcallback/) Wert. |

