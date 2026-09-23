---
title: "ReplacerContext"
linktitle: "ReplacerContext"
second_title: "Aspose.Words pour Java"
description: "Contexte d'opération de recherche/remplacement en Java."
type: docs
weight: 568
url: /fr/java/com.aspose.words/replacercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ReplacerContext extends ProcessorContext
```

Contexte d'opération de recherche/remplacement.

 **Examples:** 

Montre comment remplacer une chaîne dans le document en utilisant le contexte.

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

Montre comment remplacer une chaîne dans le document en utilisant des documents provenant du flux en utilisant le contexte.

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

Montre comment remplacer une chaîne avec une expression régulière dans le document en utilisant le contexte.

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

Montre comment remplacer une chaîne avec une expression régulière dans le document en utilisant des documents provenant du flux en utilisant le contexte.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [ReplacerContext()](#ReplacerContext) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [getFindReplaceOptions()](#getFindReplaceOptions) | Options de recherche/remplacement. |
| [getFontSettings()](#getFontSettings) | Paramètres de police utilisés par le processeur. |
| [getLayoutOptions()](#getLayoutOptions) | Options de mise en page du document utilisées par le processeur. |
| [getWarningCallback()](#getWarningCallback) | Rappel d'avertissement utilisé par le processeur. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Paramètres de police utilisés par le processeur. |
| [setReplacement(String pattern, String replacement)](#setReplacement-java.lang.String-java.lang.String) | Définit le motif et le remplacement utilisés par l'opération de recherche/remplacement. |
| [setReplacement(Pattern pattern, String replacement)](#setReplacement-java.util.regex.Pattern-java.lang.String) | Définit le motif et le remplacement utilisés par l'opération de recherche/remplacement. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Rappel d'avertissement utilisé par le processeur. |
### ReplacerContext() {#ReplacerContext}
```
public ReplacerContext()
```


Initialise une nouvelle instance de cette classe.

### getFindReplaceOptions() {#getFindReplaceOptions}
```
public FindReplaceOptions getFindReplaceOptions()
```


Options de recherche/remplacement.

 **Examples:** 

Montre comment remplacer une chaîne dans le document en utilisant le contexte.

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

Montre comment remplacer une chaîne dans le document en utilisant des documents provenant du flux en utilisant le contexte.

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

Montre comment remplacer une chaîne avec une expression régulière dans le document en utilisant le contexte.

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

Montre comment remplacer une chaîne avec une expression régulière dans le document en utilisant des documents provenant du flux en utilisant le contexte.

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


Paramètres de police utilisés par le processeur.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Options de mise en page du document utilisées par le processeur.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
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

### setReplacement(String pattern, String replacement) {#setReplacement-java.lang.String-java.lang.String}
```
public void setReplacement(String pattern, String replacement)
```


Définit le motif et le remplacement utilisés par l'opération de recherche/remplacement.

 **Remarks:** 

L'utilisation de cette méthode remplace le motif et le remplacement précédemment définis.

 **Examples:** 

Montre comment remplacer une chaîne dans le document en utilisant le contexte.

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

Montre comment remplacer une chaîne dans le document en utilisant des documents provenant du flux en utilisant le contexte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| motif | java.lang.String |  |
| remplacement | java.lang.String |  |

### setReplacement(Pattern pattern, String replacement) {#setReplacement-java.util.regex.Pattern-java.lang.String}
```
public void setReplacement(Pattern pattern, String replacement)
```


Définit le motif et le remplacement utilisés par l'opération de recherche/remplacement.

 **Remarks:** 

L'utilisation de cette méthode remplace le motif et le remplacement précédemment définis.

 **Examples:** 

Montre comment remplacer une chaîne avec une expression régulière dans le document en utilisant le contexte.

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

Montre comment remplacer une chaîne avec une expression régulière dans le document en utilisant des documents provenant du flux en utilisant le contexte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| motif | java.util.regex.Pattern |  |
| remplacement | java.lang.String |  |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Rappel d'avertissement utilisé par le processeur.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | La valeur correspondante de [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

