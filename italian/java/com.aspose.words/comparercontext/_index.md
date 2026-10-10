---
title: "ComparerContext"
linktitle: "ComparerContext"
second_title: "Aspose.Words per Java"
description: "Contesto del comparatore di documenti in Java."
type: docs
weight: 115
url: /it/java/com.aspose.words/comparercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ComparerContext extends ProcessorContext
```

Contesto del comparatore di documenti

 **Examples:** 

Mostra come confrontare semplicemente i documenti usando il contesto.

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

Mostra come confrontare i documenti dallo stream usando il contesto.

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
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [ComparerContext()](#ComparerContext) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getAcceptRevisions()](#getAcceptRevisions) | Indica se accettare le revisioni nei documenti prima di confrontarli. |
| [getAuthor()](#getAuthor) | L'autore da assegnare alle revisioni create durante il confronto dei documenti. |
| [getCompareOptions()](#getCompareOptions) | Opzioni utilizzate durante il confronto dei documenti. |
| [getDateTime()](#getDateTime) | La data e l'ora assegnate alle revisioni create durante il confronto dei documenti. |
| [getFontSettings()](#getFontSettings) | Impostazioni dei caratteri utilizzate dal processore. |
| [getLayoutOptions()](#getLayoutOptions) | Opzioni di layout del documento utilizzate dal processore. |
| [getWarningCallback()](#getWarningCallback) | Callback di avviso utilizzato dal processore. |
| [setAcceptRevisions(boolean value)](#setAcceptRevisions-boolean) | Indica se accettare le revisioni nei documenti prima di confrontarli. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | L'autore da assegnare alle revisioni create durante il confronto dei documenti. |
| [setDateTime(Date value)](#setDateTime-java.util.Date) | La data e l'ora assegnate alle revisioni create durante il confronto dei documenti. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Impostazioni dei caratteri utilizzate dal processore. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Callback di avviso utilizzato dal processore. |
### ComparerContext() {#ComparerContext}
```
public ComparerContext()
```


Inizializza una nuova istanza di questa classe.

### getAcceptRevisions() {#getAcceptRevisions}
```
public boolean getAcceptRevisions()
```


Indica se accettare le revisioni nei documenti prima di confrontarli. Se i documenti confrontati contengono revisioni e questo flag è impostato su false, il processore rifiuterà le revisioni. Il valore predefinito è  true .

**Returns:**
boolean - Il valore booleano corrispondente.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


L'autore da assegnare alle revisioni create durante il confronto dei documenti.

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getCompareOptions() {#getCompareOptions}
```
public CompareOptions getCompareOptions()
```


Opzioni utilizzate durante il confronto dei documenti.

 **Examples:** 

Mostra come confrontare semplicemente i documenti usando il contesto.

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

Mostra come confrontare i documenti dallo stream usando il contesto.

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


La data e l'ora assegnate alle revisioni create durante il confronto dei documenti.

**Returns:**
java.util.Date - Il valore corrispondente di java.util.Date.
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
### setAcceptRevisions(boolean value) {#setAcceptRevisions-boolean}
```
public void setAcceptRevisions(boolean value)
```


Indica se accettare le revisioni nei documenti prima di confrontarli. Se i documenti confrontati contengono revisioni e questo flag è impostato su false, il processore rifiuterà le revisioni. Il valore predefinito è  true .

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


L'autore da assegnare alle revisioni create durante il confronto dei documenti.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setDateTime(Date value) {#setDateTime-java.util.Date}
```
public void setDateTime(Date value)
```


La data e l'ora assegnate alle revisioni create durante il confronto dei documenti.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.util.Date | Il valore corrispondente java.util.Date. |

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

