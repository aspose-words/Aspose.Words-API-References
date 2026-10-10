---
title: "ConverterContext"
linktitle: "ConverterContext"
second_title: "Aspose.Words para Java"
description: "Contexto del convertidor de documentos en Java."
type: docs
weight: 133
url: /es/java/com.aspose.words/convertercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ConverterContext extends ProcessorContext
```

Contexto del convertidor de documentos

 **Examples:** 

Muestra cómo convertir documentos con una sola línea de código usando el contexto.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

Muestra cómo convertir documentos del flujo con una sola línea de código usando el contexto.

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```
## Métodos

| Método | Descripción |
| --- | --- |
| [getFontSettings()](#getFontSettings) | Configuración de fuentes utilizada por el procesador. |
| [getLayoutOptions()](#getLayoutOptions) | Opciones de diseño del documento utilizadas por el procesador. |
| [getWarningCallback()](#getWarningCallback) | Callback de advertencia utilizado por el procesador. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Configuración de fuentes utilizada por el procesador. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Callback de advertencia utilizado por el procesador. |
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

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Callback de advertencia utilizado por el procesador.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | El valor correspondiente de [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

