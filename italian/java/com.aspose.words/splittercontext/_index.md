---
title: "SplitterContext"
linktitle: "SplitterContext"
second_title: "Aspose.Words per Java"
description: "Contesto dello splitter di documenti in Java."
type: docs
weight: 632
url: /it/java/com.aspose.words/splittercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SplitterContext extends ProcessorContext
```

Contesto del separatore di documenti.

 **Examples:** 

Mostra come dividere il documento in pagine usando il contesto.

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

Mostra come dividere il documento dallo stream in pagine usando il contesto.

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
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [SplitterContext()](#SplitterContext) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getFontSettings()](#getFontSettings) | Impostazioni dei caratteri utilizzate dal processore. |
| [getLayoutOptions()](#getLayoutOptions) | Opzioni di layout del documento utilizzate dal processore. |
| [getSplitOptions()](#getSplitOptions) | Opzioni di divisione del documento. |
| [getWarningCallback()](#getWarningCallback) | Callback di avviso utilizzato dal processore. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Impostazioni dei caratteri utilizzate dal processore. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Callback di avviso utilizzato dal processore. |
### SplitterContext() {#SplitterContext}
```
public SplitterContext()
```


Inizializza una nuova istanza di questa classe.

### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Impostazioni dei caratteri utilizzate dal processore.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Opzioni di layout del documento utilizzate dal processore.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getSplitOptions() {#getSplitOptions}
```
public SplitOptions getSplitOptions()
```


Opzioni di divisione del documento.

 **Examples:** 

Mostra come dividere il documento in pagine usando il contesto.

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

Mostra come dividere il documento dallo stream in pagine usando il contesto.

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

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Callback di avviso utilizzato dal processore.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Il valore corrispondente di [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

