---
title: "WatermarkerContext"
linktitle: "WatermarkerContext"
second_title: "Aspose.Words pour Java"
description: "Contexte du watermarker de document en Java."
type: docs
weight: 725
url: /fr/java/com.aspose.words/watermarkercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class WatermarkerContext extends ProcessorContext
```

Contexte du filigraneur de document.

 **Examples:** 

Montre comment insérer du texte de filigrane dans le document en utilisant le contexte.

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

Montre comment insérer du texte de filigrane dans le document depuis le flux en utilisant le contexte.

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

Montre comment insérer une image de filigrane dans le document en utilisant le contexte.

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

Montre comment insérer une image de filigrane dans le document depuis un flux en utilisant le contexte.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [WatermarkerContext()](#WatermarkerContext) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [getFontSettings()](#getFontSettings) | Paramètres de police utilisés par le processeur. |
| [getImageWatermark()](#getImageWatermark) | Octets d'image à utiliser comme filigrane. |
| [getImageWatermarkOptions()](#getImageWatermarkOptions) | Options pour le filigrane texte. |
| [getLayoutOptions()](#getLayoutOptions) | Options de mise en page du document utilisées par le processeur. |
| [getTextWatermark()](#getTextWatermark) | Texte à utiliser comme filigrane. |
| [getTextWatermarkOptions()](#getTextWatermarkOptions) | Options pour le filigrane image. |
| [getWarningCallback()](#getWarningCallback) | Rappel d'avertissement utilisé par le processeur. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Paramètres de police utilisés par le processeur. |
| [setImageWatermark(byte[] value)](#setImageWatermark-byte) | Octets d'image à utiliser comme filigrane. |
| [setTextWatermark(String value)](#setTextWatermark-java.lang.String) | Texte à utiliser comme filigrane. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Rappel d'avertissement utilisé par le processeur. |
### WatermarkerContext() {#WatermarkerContext}
```
public WatermarkerContext()
```


Initialise une nouvelle instance de cette classe.

### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Paramètres de police utilisés par le processeur.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getImageWatermark() {#getImageWatermark}
```
public byte[] getImageWatermark()
```


Octets d'image à utiliser comme filigrane.

 **Remarks:** 

Si les deux [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) et [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) sont spécifiés, le filigrane texte remplace le filigrane image.

 **Examples:** 

Montre comment insérer une image de filigrane dans le document en utilisant le contexte.

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

Montre comment insérer une image de filigrane dans le document depuis un flux en utilisant le contexte.

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
byte[] - La valeur byte[] correspondante.
### getImageWatermarkOptions() {#getImageWatermarkOptions}
```
public ImageWatermarkOptions getImageWatermarkOptions()
```


Options pour le filigrane texte.

 **Examples:** 

Montre comment insérer une image de filigrane dans le document en utilisant le contexte.

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

Montre comment insérer une image de filigrane dans le document depuis un flux en utilisant le contexte.

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


Options de mise en page du document utilisées par le processeur.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getTextWatermark() {#getTextWatermark}
```
public String getTextWatermark()
```


Texte à utiliser comme filigrane.

 **Remarks:** 

Si les deux [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) et [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) sont spécifiés, le filigrane texte remplace le filigrane image.

 **Examples:** 

Montre comment insérer du texte de filigrane dans le document en utilisant le contexte.

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

Montre comment insérer du texte de filigrane dans le document depuis le flux en utilisant le contexte.

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
java.lang.String - La valeur java.lang.String correspondante.
### getTextWatermarkOptions() {#getTextWatermarkOptions}
```
public TextWatermarkOptions getTextWatermarkOptions()
```


Options pour le filigrane image.

 **Examples:** 

Montre comment insérer du texte de filigrane dans le document en utilisant le contexte.

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

Montre comment insérer du texte de filigrane dans le document depuis le flux en utilisant le contexte.

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


Rappel d'avertissement utilisé par le processeur.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Paramètres de police utilisés par le processeur.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | La valeur correspondante de [FontSettings](../../com.aspose.words/fontsettings/). |

### setImageWatermark(byte[] value) {#setImageWatermark-byte}
```
public void setImageWatermark(byte[] value)
```


Octets d'image à utiliser comme filigrane.

 **Remarks:** 

Si les deux [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) et [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) sont spécifiés, le filigrane texte remplace le filigrane image.

 **Examples:** 

Montre comment insérer une image de filigrane dans le document en utilisant le contexte.

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

Montre comment insérer une image de filigrane dans le document depuis un flux en utilisant le contexte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | byte[] | La valeur byte[] correspondante. |

### setTextWatermark(String value) {#setTextWatermark-java.lang.String}
```
public void setTextWatermark(String value)
```


Texte à utiliser comme filigrane.

 **Remarks:** 

Si les deux [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) et [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) sont spécifiés, le filigrane texte remplace le filigrane image.

 **Examples:** 

Montre comment insérer du texte de filigrane dans le document en utilisant le contexte.

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

Montre comment insérer du texte de filigrane dans le document depuis le flux en utilisant le contexte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Rappel d'avertissement utilisé par le processeur.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | La valeur correspondante de [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

