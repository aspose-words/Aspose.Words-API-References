---
title: SplitterContext
linktitle: SplitterContext
second_title: Aspose.Words for Java
description: Document splitter context in Java.
type: docs
weight: 624
url: /java/com.aspose.words/splittercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SplitterContext extends ProcessorContext
```

Document splitter context.

 **Examples:** 

Shows how to split document by pages using context.

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

Shows how to split document from the stream by pages using context.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [SplitterContext()](#SplitterContext) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getFontSettings()](#getFontSettings) | Font settings used by the processor. |
| [getLayoutOptions()](#getLayoutOptions) | Document layout options used by the processor. |
| [getSplitOptions()](#getSplitOptions) | Document split options. |
| [getWarningCallback()](#getWarningCallback) | Warning callback used by the processor. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Font settings used by the processor. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Warning callback used by the processor. |
### SplitterContext() {#SplitterContext}
```
public SplitterContext()
```


Initializes a new instance of this class.

### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Font settings used by the processor.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Document layout options used by the processor.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getSplitOptions() {#getSplitOptions}
```
public SplitOptions getSplitOptions()
```


Document split options.

 **Examples:** 

Shows how to split document by pages using context.

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

Shows how to split document from the stream by pages using context.

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


Warning callback used by the processor.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Font settings used by the processor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Warning callback used by the processor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value. |

