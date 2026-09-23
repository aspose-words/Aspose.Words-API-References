---
title: "SplitterContext"
linktitle: "SplitterContext"
second_title: "Aspose.Words für Java"
description: "Dokumenten‑Splitter‑Kontext in Java."
type: docs
weight: 632
url: /de/java/com.aspose.words/splittercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SplitterContext extends ProcessorContext
```

Kontext des Dokumententeilers.

 **Examples:** 

Zeigt, wie man ein Dokument mithilfe des Kontexts nach Seiten aufteilt.

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

Zeigt, wie man ein Dokument aus dem Stream nach Seiten mithilfe des Kontexts aufteilt.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [SplitterContext()](#SplitterContext) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getFontSettings()](#getFontSettings) | Schrifteinstellungen, die vom Prozessor verwendet werden. |
| [getLayoutOptions()](#getLayoutOptions) | Dokumentenlayout‑Optionen, die vom Prozessor verwendet werden. |
| [getSplitOptions()](#getSplitOptions) | Optionen zum Aufteilen des Dokuments. |
| [getWarningCallback()](#getWarningCallback) | Warn‑Callback, das vom Prozessor verwendet wird. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Schrifteinstellungen, die vom Prozessor verwendet werden. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Warn‑Callback, das vom Prozessor verwendet wird. |
### SplitterContext() {#SplitterContext}
```
public SplitterContext()
```


Initialisiert eine neue Instanz dieser Klasse.

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
### getSplitOptions() {#getSplitOptions}
```
public SplitOptions getSplitOptions()
```


Optionen zum Aufteilen des Dokuments.

 **Examples:** 

Zeigt, wie man ein Dokument mithilfe des Kontexts nach Seiten aufteilt.

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

Zeigt, wie man ein Dokument aus dem Stream nach Seiten mithilfe des Kontexts aufteilt.

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

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Warn‑Callback, das vom Prozessor verwendet wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Der entsprechende [IWarningCallback](../../com.aspose.words/iwarningcallback/) Wert. |

