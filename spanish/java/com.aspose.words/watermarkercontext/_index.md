---
title: "WatermarkerContext"
linktitle: "WatermarkerContext"
second_title: "Aspose.Words para Java"
description: "Contexto de marcador de agua de documento en Java."
type: docs
weight: 725
url: /es/java/com.aspose.words/watermarkercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class WatermarkerContext extends ProcessorContext
```

Contexto del marcador de agua del documento.

 **Examples:** 

Muestra cómo insertar texto de marca de agua en el documento usando el contexto.

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

Muestra cómo insertar texto de marca de agua en el documento desde el flujo usando el contexto.

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

Muestra cómo insertar una imagen de marca de agua en el documento usando el contexto.

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

Muestra cómo insertar una imagen de marca de agua en el documento desde un flujo usando el contexto.

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [WatermarkerContext()](#WatermarkerContext) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getFontSettings()](#getFontSettings) | Configuración de fuentes utilizada por el procesador. |
| [getImageWatermark()](#getImageWatermark) | Bytes de imagen que se usarán como marca de agua. |
| [getImageWatermarkOptions()](#getImageWatermarkOptions) | Opciones para la marca de agua de texto. |
| [getLayoutOptions()](#getLayoutOptions) | Opciones de diseño del documento utilizadas por el procesador. |
| [getTextWatermark()](#getTextWatermark) | Texto que se usará como marca de agua. |
| [getTextWatermarkOptions()](#getTextWatermarkOptions) | Opciones para la marca de agua de imagen. |
| [getWarningCallback()](#getWarningCallback) | Callback de advertencia utilizado por el procesador. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Configuración de fuentes utilizada por el procesador. |
| [setImageWatermark(byte[] value)](#setImageWatermark-byte) | Bytes de imagen que se usarán como marca de agua. |
| [setTextWatermark(String value)](#setTextWatermark-java.lang.String) | Texto que se usará como marca de agua. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Callback de advertencia utilizado por el procesador. |
### WatermarkerContext() {#WatermarkerContext}
```
public WatermarkerContext()
```


Inicializa una nueva instancia de esta clase.

### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Configuración de fuentes utilizada por el procesador.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getImageWatermark() {#getImageWatermark}
```
public byte[] getImageWatermark()
```


Bytes de imagen que se usarán como marca de agua.

 **Remarks:** 

Si se especifican tanto [getImageWatermark()](../../com.aspose.words/watermarkercontext/\\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\\#setImageWatermark-byte) como [getTextWatermark()](../../com.aspose.words/watermarkercontext/\\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\\#setTextWatermark-java.lang.String), la marca de agua de texto sobrescribe la marca de agua de imagen.

 **Examples:** 

Muestra cómo insertar una imagen de marca de agua en el documento usando el contexto.

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

Muestra cómo insertar una imagen de marca de agua en el documento desde un flujo usando el contexto.

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
byte[] - El valor byte[] correspondiente.
### getImageWatermarkOptions() {#getImageWatermarkOptions}
```
public ImageWatermarkOptions getImageWatermarkOptions()
```


Opciones para la marca de agua de texto.

 **Examples:** 

Muestra cómo insertar una imagen de marca de agua en el documento usando el contexto.

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

Muestra cómo insertar una imagen de marca de agua en el documento desde un flujo usando el contexto.

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


Opciones de diseño del documento utilizadas por el procesador.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getTextWatermark() {#getTextWatermark}
```
public String getTextWatermark()
```


Texto que se usará como marca de agua.

 **Remarks:** 

Si se especifican tanto [getImageWatermark()](../../com.aspose.words/watermarkercontext/\\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\\#setImageWatermark-byte) como [getTextWatermark()](../../com.aspose.words/watermarkercontext/\\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\\#setTextWatermark-java.lang.String), la marca de agua de texto sobrescribe la marca de agua de imagen.

 **Examples:** 

Muestra cómo insertar texto de marca de agua en el documento usando el contexto.

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

Muestra cómo insertar texto de marca de agua en el documento desde el flujo usando el contexto.

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
java.lang.String - El valor java.lang.String correspondiente.
### getTextWatermarkOptions() {#getTextWatermarkOptions}
```
public TextWatermarkOptions getTextWatermarkOptions()
```


Opciones para la marca de agua de imagen.

 **Examples:** 

Muestra cómo insertar texto de marca de agua en el documento usando el contexto.

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

Muestra cómo insertar texto de marca de agua en el documento desde el flujo usando el contexto.

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


Callback de advertencia utilizado por el procesador.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Configuración de fuentes utilizada por el procesador.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | El valor correspondiente de [FontSettings](../../com.aspose.words/fontsettings/). |

### setImageWatermark(byte[] value) {#setImageWatermark-byte}
```
public void setImageWatermark(byte[] value)
```


Bytes de imagen que se usarán como marca de agua.

 **Remarks:** 

Si se especifican tanto [getImageWatermark()](../../com.aspose.words/watermarkercontext/\\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\\#setImageWatermark-byte) como [getTextWatermark()](../../com.aspose.words/watermarkercontext/\\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\\#setTextWatermark-java.lang.String), la marca de agua de texto sobrescribe la marca de agua de imagen.

 **Examples:** 

Muestra cómo insertar una imagen de marca de agua en el documento usando el contexto.

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

Muestra cómo insertar una imagen de marca de agua en el documento desde un flujo usando el contexto.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | byte[] | El valor byte[] correspondiente. |

### setTextWatermark(String value) {#setTextWatermark-java.lang.String}
```
public void setTextWatermark(String value)
```


Texto que se usará como marca de agua.

 **Remarks:** 

Si se especifican tanto [getImageWatermark()](../../com.aspose.words/watermarkercontext/\\#getImageWatermark) / [setImageWatermark(byte[])](../../com.aspose.words/watermarkercontext/\\#setImageWatermark-byte) como [getTextWatermark()](../../com.aspose.words/watermarkercontext/\\#getTextWatermark) / [setTextWatermark(java.lang.String)](../../com.aspose.words/watermarkercontext/\\#setTextWatermark-java.lang.String), la marca de agua de texto sobrescribe la marca de agua de imagen.

 **Examples:** 

Muestra cómo insertar texto de marca de agua en el documento usando el contexto.

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

Muestra cómo insertar texto de marca de agua en el documento desde el flujo usando el contexto.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Callback de advertencia utilizado por el procesador.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | El valor correspondiente de [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

