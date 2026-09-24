---
title: "MergerContext"
linktitle: "MergerContext"
second_title: "Aspose.Words para Java"
description: "Contexto de fusión de documentos en Java."
type: docs
weight: 466
url: /es/java/com.aspose.words/mergercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class MergerContext extends ProcessorContext
```

Contexto del combinador de documentos.

 **Examples:** 

Muestra cómo combinar documentos en un único documento de salida usando el contexto.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

Muestra cómo combinar documentos del flujo en un único documento de salida usando el contexto.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```
## Métodos

| Método | Descripción |
| --- | --- |
| [getFontSettings()](#getFontSettings) | Configuración de fuentes utilizada por el procesador. |
| [getLayoutOptions()](#getLayoutOptions) | Opciones de diseño del documento utilizadas por el procesador. |
| [getMergeFormatMode()](#getMergeFormatMode) | Especifica cómo fusionar el formato que entra en conflicto. |
| [getWarningCallback()](#getWarningCallback) | Callback de advertencia utilizado por el procesador. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Configuración de fuentes utilizada por el procesador. |
| [setMergeFormatMode(int value)](#setMergeFormatMode-int) | Especifica cómo fusionar el formato que entra en conflicto. |
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
### getMergeFormatMode() {#getMergeFormatMode}
```
public int getMergeFormatMode()
```


Especifica cómo fusionar el formato que entra en conflicto.

**Returns:**
int - El valor  int  correspondiente. El valor devuelto es uno de los constantes de [MergeFormatMode](../../com.aspose.words/mergeformatmode/).
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

### setMergeFormatMode(int value) {#setMergeFormatMode-int}
```
public void setMergeFormatMode(int value)
```


Especifica cómo fusionar el formato que entra en conflicto.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor  int  correspondiente. El valor debe ser uno de los constantes de [MergeFormatMode](../../com.aspose.words/mergeformatmode/). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Callback de advertencia utilizado por el procesador.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | El valor correspondiente de [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

