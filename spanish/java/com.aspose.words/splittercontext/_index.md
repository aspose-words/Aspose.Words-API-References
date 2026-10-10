---
title: "SplitterContext"
linktitle: "SplitterContext"
second_title: "Aspose.Words para Java"
description: "Contexto del divisor de documentos en Java."
type: docs
weight: 632
url: /es/java/com.aspose.words/splittercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SplitterContext extends ProcessorContext
```

Contexto del divisor de documentos.

 **Examples:** 

Muestra cómo dividir el documento por páginas usando el contexto.

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

Muestra cómo dividir el documento desde el flujo por páginas usando el contexto.

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx")) {
     SplitterContext splitterContext = new SplitterContext();
     splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

     ArrayList pages = new ArrayList<>();
     Splitter.create(splitterContext)
             .from(streamIn)
             .toOutput(pages, SaveFormat.DOCX)
             .execute();
 }
 
```
## Constructores

| Constructor | Descripción |
| --- | --- |
| [SplitterContext()](#SplitterContext) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getFontSettings()](#getFontSettings) | Configuración de fuentes utilizada por el procesador. |
| [getLayoutOptions()](#getLayoutOptions) | Opciones de diseño del documento utilizadas por el procesador. |
| [getSplitOptions()](#getSplitOptions) | Opciones de división del documento. |
| [getWarningCallback()](#getWarningCallback) | Callback de advertencia utilizado por el procesador. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Configuración de fuentes utilizada por el procesador. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Callback de advertencia utilizado por el procesador. |
### SplitterContext() {#SplitterContext}
```
public SplitterContext()
```


Inicializa una nueva instancia de esta clase.

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
### getSplitOptions() {#getSplitOptions}
```
public SplitOptions getSplitOptions()
```


Opciones de división del documento.

 **Examples:** 

Muestra cómo dividir el documento por páginas usando el contexto.

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

Muestra cómo dividir el documento desde el flujo por páginas usando el contexto.

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx")) {
     SplitterContext splitterContext = new SplitterContext();
     splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

     ArrayList pages = new ArrayList<>();
     Splitter.create(splitterContext)
             .from(streamIn)
             .toOutput(pages, SaveFormat.DOCX)
             .execute();
 }
 
```

**Returns:**
[SplitOptions](../../com.aspose.words/splitoptions/) - The corresponding [SplitOptions](../../com.aspose.words/splitoptions/) value.
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

