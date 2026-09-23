---
title: "ReplacerContext"
linktitle: "ReplacerContext"
second_title: "Aspose.Words per Java"
description: "Contesto dell'operazione di ricerca/sostituzione in Java."
type: docs
weight: 568
url: /it/java/com.aspose.words/replacercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ReplacerContext extends ProcessorContext
```

Contesto dell'operazione di ricerca/sostituzione.

 **Examples:** 

Mostra come sostituire una stringa nel documento utilizzando il contesto.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContext.docx")
         .execute();
 
```

Mostra come sostituire una stringa nel documento utilizzando documenti dallo stream con il contesto.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStream.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

Mostra come sostituire una stringa con regex nel documento utilizzando il contesto.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContextRegex.docx")
         .execute();
 
```

Mostra come sostituire una stringa con regex nel documento utilizzando documenti dallo stream con il contesto.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStreamRegex.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [ReplacerContext()](#ReplacerContext) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getFindReplaceOptions()](#getFindReplaceOptions) | Opzioni di ricerca/sostituzione. |
| [getFontSettings()](#getFontSettings) | Impostazioni dei caratteri utilizzate dal processore. |
| [getLayoutOptions()](#getLayoutOptions) | Opzioni di layout del documento utilizzate dal processore. |
| [getWarningCallback()](#getWarningCallback) | Callback di avviso utilizzato dal processore. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Impostazioni dei caratteri utilizzate dal processore. |
| [setReplacement(String pattern, String replacement)](#setReplacement-java.lang.String-java.lang.String) | Imposta il modello e la sostituzione utilizzati dall'operazione di ricerca/sostituzione. |
| [setReplacement(Pattern pattern, String replacement)](#setReplacement-java.util.regex.Pattern-java.lang.String) | Imposta il modello e la sostituzione utilizzati dall'operazione di ricerca/sostituzione. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Callback di avviso utilizzato dal processore. |
### ReplacerContext() {#ReplacerContext}
```
public ReplacerContext()
```


Inizializza una nuova istanza di questa classe.

### getFindReplaceOptions() {#getFindReplaceOptions}
```
public FindReplaceOptions getFindReplaceOptions()
```


Opzioni di ricerca/sostituzione.

 **Examples:** 

Mostra come sostituire una stringa nel documento utilizzando il contesto.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContext.docx")
         .execute();
 
```

Mostra come sostituire una stringa nel documento utilizzando documenti dallo stream con il contesto.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStream.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

Mostra come sostituire una stringa con regex nel documento utilizzando il contesto.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContextRegex.docx")
         .execute();
 
```

Mostra come sostituire una stringa con regex nel documento utilizzando documenti dallo stream con il contesto.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStreamRegex.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
[FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) - The corresponding [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) value.
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

### setReplacement(String pattern, String replacement) {#setReplacement-java.lang.String-java.lang.String}
```
public void setReplacement(String pattern, String replacement)
```


Imposta il modello e la sostituzione utilizzati dall'operazione di ricerca/sostituzione.

 **Remarks:** 

L'utilizzo di questo metodo sovrascrive il modello e la sostituzione impostati in precedenza.

 **Examples:** 

Mostra come sostituire una stringa nel documento utilizzando il contesto.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContext.docx")
         .execute();
 
```

Mostra come sostituire una stringa nel documento utilizzando documenti dallo stream con il contesto.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStream.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| modello | java.lang.String |  |
| sostituzione | java.lang.String |  |

### setReplacement(Pattern pattern, String replacement) {#setReplacement-java.util.regex.Pattern-java.lang.String}
```
public void setReplacement(Pattern pattern, String replacement)
```


Imposta il modello e la sostituzione utilizzati dall'operazione di ricerca/sostituzione.

 **Remarks:** 

L'utilizzo di questo metodo sovrascrive il modello e la sostituzione impostati in precedenza.

 **Examples:** 

Mostra come sostituire una stringa con regex nel documento utilizzando il contesto.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContextRegex.docx")
         .execute();
 
```

Mostra come sostituire una stringa con regex nel documento utilizzando documenti dallo stream con il contesto.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStreamRegex.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| modello | java.util.regex.Pattern |  |
| sostituzione | java.lang.String |  |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Callback di avviso utilizzato dal processore.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Il valore corrispondente di [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

