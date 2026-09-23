---
title: "ComparerContext"
linktitle: "ComparerContext"
second_title: "Aspose.Words pour Java"
description: "Contexte du comparateur de documents en Java."
type: docs
weight: 115
url: /fr/java/com.aspose.words/comparercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ComparerContext extends ProcessorContext
```

Contexte du comparateur de documents

 **Examples:** 

Montre comment comparer simplement des documents en utilisant le contexte.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

Montre comment comparer des documents depuis le flux en utilisant le contexte.

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```
## Constructors

| Constructor | Description |
| --- | --- |
| [ComparerContext()](#ComparerContext) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [getAcceptRevisions()](#getAcceptRevisions) | Indique s'il faut accepter les révisions dans les documents avant de les comparer. |
| [getAuthor()](#getAuthor) | L'auteur à attribuer aux révisions créées lors de la comparaison de documents. |
| [getCompareOptions()](#getCompareOptions) | Options utilisées lors de la comparaison de documents. |
| [getDateTime()](#getDateTime) | La date et l'heure attribuées aux révisions créées lors de la comparaison de documents. |
| [getFontSettings()](#getFontSettings) | Paramètres de police utilisés par le processeur. |
| [getLayoutOptions()](#getLayoutOptions) | Options de mise en page du document utilisées par le processeur. |
| [getWarningCallback()](#getWarningCallback) | Rappel d'avertissement utilisé par le processeur. |
| [setAcceptRevisions(boolean value)](#setAcceptRevisions-boolean) | Indique s'il faut accepter les révisions dans les documents avant de les comparer. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | L'auteur à attribuer aux révisions créées lors de la comparaison de documents. |
| [setDateTime(Date value)](#setDateTime-java.util.Date) | La date et l'heure attribuées aux révisions créées lors de la comparaison de documents. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Paramètres de police utilisés par le processeur. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Rappel d'avertissement utilisé par le processeur. |
### ComparerContext() {#ComparerContext}
```
public ComparerContext()
```


Initialise une nouvelle instance de cette classe.

### getAcceptRevisions() {#getAcceptRevisions}
```
public boolean getAcceptRevisions()
```


Indique s'il faut accepter les révisions dans les documents avant de les comparer. Si les documents comparés contiennent des révisions et que ce drapeau est réglé sur false, le processeur rejettera les révisions. La valeur par défaut est  true .

**Returns:**
boolean - La valeur  boolean  correspondante.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


L'auteur à attribuer aux révisions créées lors de la comparaison de documents.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getCompareOptions() {#getCompareOptions}
```
public CompareOptions getCompareOptions()
```


Options utilisées lors de la comparaison de documents.

 **Examples:** 

Montre comment comparer simplement des documents en utilisant le contexte.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

Montre comment comparer des documents depuis le flux en utilisant le contexte.

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

**Returns:**
[CompareOptions](../../com.aspose.words/compareoptions/) - The corresponding [CompareOptions](../../com.aspose.words/compareoptions/) value.
### getDateTime() {#getDateTime}
```
public Date getDateTime()
```


La date et l'heure attribuées aux révisions créées lors de la comparaison de documents.

**Returns:**
java.util.Date - La valeur java.util.Date correspondante.
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
### setAcceptRevisions(boolean value) {#setAcceptRevisions-boolean}
```
public void setAcceptRevisions(boolean value)
```


Indique s'il faut accepter les révisions dans les documents avant de les comparer. Si les documents comparés contiennent des révisions et que ce drapeau est réglé sur false, le processeur rejettera les révisions. La valeur par défaut est  true .

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


L'auteur à attribuer aux révisions créées lors de la comparaison de documents.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setDateTime(Date value) {#setDateTime-java.util.Date}
```
public void setDateTime(Date value)
```


La date et l'heure attribuées aux révisions créées lors de la comparaison de documents.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.util.Date | La valeur java.util.Date correspondante. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Paramètres de police utilisés par le processeur.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | La valeur correspondante de [FontSettings](../../com.aspose.words/fontsettings/). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Rappel d'avertissement utilisé par le processeur.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | La valeur correspondante de [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

