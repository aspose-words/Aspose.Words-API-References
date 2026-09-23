---
title: "WatermarkerContext"
linktitle: "WatermarkerContext"
second_title: "Aspose.Words per Java"
description: "Contesto di watermarker del documento in Java."
type: docs
weight: 725
url: /it/java/com.aspose.words/watermarkercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class WatermarkerContext extends ProcessorContext
```

Contesto del watermarker del documento.

 **Examples:** 

Mostra come inserire testo di filigrana nel documento usando il contesto.

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

Mostra come inserire il testo di filigrana nel documento dallo stream usando il contesto.

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

Mostra come inserire l'immagine di filigrana nel documento usando il contesto.

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

Mostra come inserire l'immagine di filigrana nel documento da uno stream usando il contesto.

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
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [WatermarkerContext()](#WatermarkerContext) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getFontSettings()](#getFontSettings) | Impostazioni dei caratteri utilizzate dal processore. |
| [getImageWatermark()](#getImageWatermark) | Byte dell'immagine da utilizzare come filigrana. |
| [getImageWatermarkOptions()](#getImageWatermarkOptions) | Opzioni per la filigrana di testo. |
| [getLayoutOptions()](#getLayoutOptions) | Opzioni di layout del documento utilizzate dal processore. |
| [getTextWatermark()](#getTextWatermark) | Testo da utilizzare come filigrana. |
| [getTextWatermarkOptions()](#getTextWatermarkOptions) | Opzioni per la filigrana immagine. |
| [getWarningCallback()](#getWarningCallback) | Callback di avviso utilizzato dal processore. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Impostazioni dei caratteri utilizzate dal processore. |
| [setImageWatermark(byte[] value)](#setImageWatermark-byte) | Byte dell'immagine da utilizzare come filigrana. |
| [setTextWatermark(String value)](#setTextWatermark-java.lang.String) | Testo da utilizzare come filigrana. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Callback di avviso utilizzato dal processore. |
### WatermarkerContext() {#WatermarkerContext}
```
public WatermarkerContext()
```


Inizializza una nuova istanza di questa classe.

### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Impostazioni dei caratteri utilizzate dal processore.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getImageWatermark() {#getImageWatermark}
```
public byte[] getImageWatermark()
```


Byte dell'immagine da utilizzare come filigrana.

 **Remarks:** 

Se sia [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) e [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) sono specificati, la filigrana di testo sovrascrive la filigrana immagine.

 **Examples:** 

Mostra come inserire l'immagine di filigrana nel documento usando il contesto.

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

Mostra come inserire l'immagine di filigrana nel documento da uno stream usando il contesto.

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
byte[] - Il valore byte[] corrispondente.
### getImageWatermarkOptions() {#getImageWatermarkOptions}
```
public ImageWatermarkOptions getImageWatermarkOptions()
```


Opzioni per la filigrana di testo.

 **Examples:** 

Mostra come inserire l'immagine di filigrana nel documento usando il contesto.

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

Mostra come inserire l'immagine di filigrana nel documento da uno stream usando il contesto.

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


Opzioni di layout del documento utilizzate dal processore.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getTextWatermark() {#getTextWatermark}
```
public String getTextWatermark()
```


Testo da utilizzare come filigrana.

 **Remarks:** 

Se sia [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) e [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) sono specificati, la filigrana di testo sovrascrive la filigrana immagine.

 **Examples:** 

Mostra come inserire testo di filigrana nel documento usando il contesto.

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

Mostra come inserire il testo di filigrana nel documento dallo stream usando il contesto.

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
java.lang.String - Il valore java.lang.String corrispondente.
### getTextWatermarkOptions() {#getTextWatermarkOptions}
```
public TextWatermarkOptions getTextWatermarkOptions()
```


Opzioni per la filigrana immagine.

 **Examples:** 

Mostra come inserire testo di filigrana nel documento usando il contesto.

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

Mostra come inserire il testo di filigrana nel documento dallo stream usando il contesto.

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


Callback di avviso utilizzato dal processore.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Impostazioni dei caratteri utilizzate dal processore.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | Il valore corrispondente di [FontSettings](../../com.aspose.words/fontsettings/). |

### setImageWatermark(byte[] value) {#setImageWatermark-byte}
```
public void setImageWatermark(byte[] value)
```


Byte dell'immagine da utilizzare come filigrana.

 **Remarks:** 

Se sia [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) e [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) sono specificati, la filigrana di testo sovrascrive la filigrana immagine.

 **Examples:** 

Mostra come inserire l'immagine di filigrana nel documento usando il contesto.

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

Mostra come inserire l'immagine di filigrana nel documento da uno stream usando il contesto.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | byte[] | Il valore byte[] corrispondente. |

### setTextWatermark(String value) {#setTextWatermark-java.lang.String}
```
public void setTextWatermark(String value)
```


Testo da utilizzare come filigrana.

 **Remarks:** 

Se sia [getImageWatermark()](../../com.aspose.words/watermarkercontext/\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\#setImageWatermark-byte) e [getTextWatermark()](../../com.aspose.words/watermarkercontext/\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\#setTextWatermark-java.lang.String) sono specificati, la filigrana di testo sovrascrive la filigrana immagine.

 **Examples:** 

Mostra come inserire testo di filigrana nel documento usando il contesto.

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

Mostra come inserire il testo di filigrana nel documento dallo stream usando il contesto.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Callback di avviso utilizzato dal processore.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Il valore corrispondente di [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

