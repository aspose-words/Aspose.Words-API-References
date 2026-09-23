---
title: "Comparer"
linktitle: "Comparer"
second_title: "Aspose.Words per Java"
description: "Fornisce metodi destinati a confrontare documenti in Java."
type: docs
weight: 114
url: /it/java/com.aspose.words/comparer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Comparer extends Processor
```

Fornisce metodi destinati a confrontare i documenti.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date) | Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| [compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| [compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date) |  |
| [compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(String v1, String v2, String outputFileName, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date) | Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| [compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato, producendo modifiche come un numero di revisioni di modifica e formattazione. |
| [compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)](#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date) | Confronta due documenti e salva le differenze come immagini. |
| [compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Confronta due documenti e salva le differenze come immagini. |
| [compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)](#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date) | Confronta due documenti e salva le differenze come immagini. |
| [compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Confronta due documenti e salva le differenze come immagini. |
| [create()](#create) | Crea una nuova istanza del processore di conversione. |
| [create(ComparerContext context)](#create-com.aspose.words.ComparerContext) | Crea una nuova istanza del processore di confronto. |
| [execute()](#execute) | Esegui l'azione del processore. |
| [from(InputStream input)](#from-java.io.InputStream) | Specifica il documento di input per l'elaborazione. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Specifica il documento di input per l'elaborazione. |
| [from(String input)](#from-java.lang.String) | Specifica il documento di input per l'elaborazione. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Specifica il documento di input per l'elaborazione. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Specifica il file di output per il processore. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Specifica il file di output per il processore. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| autore | java.lang.String |  |
| dateTime | java.util.Date |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| autore | java.lang.String |  |
| dateTime | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| autore | java.lang.String |  |
| dateTime | java.util.Date |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| autore | java.lang.String |  |
| dateTime | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime)
```


Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formattazione.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.lang.String | Il documento originale. |
| v2 | java.lang.String | Il documento modificato. |
| outputFileName | java.lang.String | Il nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Le opzioni di salvataggio dell'output. |
| autore | java.lang.String | Iniziali dell'autore da usare per le revisioni. |
| dateTime | java.util.Date | La data e l'ora da usare per le revisioni. |

### compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato nel formato di salvataggio fornito, producendo modifiche come un numero di revisioni di modifica e formattazione.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.lang.String | Il documento originale. |
| v2 | java.lang.String | Il documento modificato. |
| outputFileName | java.lang.String | Il nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Le opzioni di salvataggio dell'output. |
| autore | java.lang.String | Iniziali dell'autore da usare per le revisioni. |
| dateTime | java.util.Date | La data e l'ora da usare per le revisioni. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Opzioni di confronto dei documenti. |

### compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.lang.String |  |
| v2 | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| autore | java.lang.String |  |
| dateTime | java.util.Date |  |

### compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.lang.String |  |
| v2 | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| autore | java.lang.String |  |
| dateTime | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(String v1, String v2, String outputFileName, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, String author, Date dateTime)
```


Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato, producendo modifiche come un numero di revisioni di modifica e formattazione.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.lang.String | Il documento originale. |
| v2 | java.lang.String | Il documento modificato. |
| outputFileName | java.lang.String | Il nome file di output. |
| autore | java.lang.String | Iniziali dell'autore da usare per le revisioni. |
| dateTime | java.util.Date | La data e l'ora da usare per le revisioni. |

### compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions)
```


Confronta due documenti con opzioni aggiuntive e salva le differenze nel file di output specificato, producendo modifiche come un numero di revisioni di modifica e formattazione.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

 **Examples:** 

Mostra come confrontare semplicemente i documenti.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.1.docx", "Author", new Date());
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.2.docx", SaveFormat.DOCX, "Author", new Date());
 CompareOptions options = new CompareOptions();
 options.setIgnoreCaseChanges(true);
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.3.docx", "Author", new Date(), options);
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.4.docx", SaveFormat.DOCX, "Author", new Date(), options);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.lang.String | Il documento originale. |
| v2 | java.lang.String | Il documento modificato. |
| outputFileName | java.lang.String | Il nome file di output. |
| autore | java.lang.String | Iniziali dell'autore da usare per le revisioni. |
| dateTime | java.util.Date | La data e l'ora da usare per le revisioni. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Opzioni di confronto dei documenti. |

### compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime) {#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date}
```
public static OutputStream[] compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)
```


Confronta due documenti e salva le differenze come immagini. Ogni elemento nell'array restituito rappresenta una singola pagina dell'output renderizzata come immagine.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.io.InputStream | Il documento originale. |
| v2 | java.io.InputStream | Il documento modificato. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio delle immagini dell'output. |
| autore | java.lang.String | Iniziali dell'autore da usare per le revisioni. |
| dateTime | java.util.Date | La data e l'ora da usare per le revisioni. |

**Returns:**
java.io.OutputStream[]
### compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static OutputStream[] compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


Confronta due documenti e salva le differenze come immagini. Ogni elemento nell'array restituito rappresenta una singola pagina dell'output renderizzata come immagine.

 **Examples:** 

Mostra come confrontare i documenti e salvare i risultati come immagini.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 OutputStream[] pages = Comparer.compareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.PNG), "Author", new Date());

 try (FileInputStream firstStreamIn = new FileInputStream(firstDoc)) {
     try (FileInputStream secondStreamIn = new FileInputStream(secondDoc)) {
         CompareOptions compareOptions = new CompareOptions();
         compareOptions.setIgnoreCaseChanges(true);
         pages = Comparer.compareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.PNG), "Author", new Date(), compareOptions);
     }
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.io.InputStream | Il documento originale. |
| v2 | java.io.InputStream | Il documento modificato. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio delle immagini dell'output. |
| autore | java.lang.String | Iniziali dell'autore da usare per le revisioni. |
| dateTime | java.util.Date | La data e l'ora da usare per le revisioni. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Opzioni di confronto dei documenti. |

**Returns:**
java.io.OutputStream[]
### compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime) {#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date}
```
public static OutputStream[] compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)
```


Confronta due documenti e salva le differenze come immagini. Ogni elemento nell'array restituito rappresenta una singola pagina dell'output renderizzata come immagine.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.lang.String | Il documento originale. |
| v2 | java.lang.String | Il documento modificato. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio delle immagini dell'output. |
| autore | java.lang.String | Iniziali dell'autore da usare per le revisioni. |
| dateTime | java.util.Date | La data e l'ora da usare per le revisioni. |

**Returns:**
java.io.OutputStream[]
### compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static OutputStream[] compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


Confronta due documenti e salva le differenze come immagini. Ogni elemento nell'array restituito rappresenta una singola pagina dell'output renderizzata come immagine.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| v1 | java.lang.String | Il documento originale. |
| v2 | java.lang.String | Il documento modificato. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Le opzioni di salvataggio delle immagini dell'output. |
| autore | java.lang.String | Iniziali dell'autore da usare per le revisioni. |
| dateTime | java.util.Date | La data e l'ora da usare per le revisioni. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Opzioni di confronto dei documenti. |

**Returns:**
java.io.OutputStream[]
### create() {#create}
```
public static Comparer create()
```


Crea una nuova istanza del processore di conversione.

**Returns:**
[Comparer](../../com.aspose.words/comparer/)
### create(ComparerContext context) {#create-com.aspose.words.ComparerContext}
```
public static Comparer create(ComparerContext context)
```


Crea una nuova istanza del processore di confronto.

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

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| context | [ComparerContext](../../com.aspose.words/comparercontext/) |  |

**Returns:**
[Comparer](../../com.aspose.words/comparer/)
### execute() {#execute}
```
public void execute()
```


Esegui l'azione del processore.

 **Examples:** 

Mostra come unire documenti in un unico documento di output usando il contesto.

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

Mostra come unire documenti dallo stream in un unico documento di output usando il contesto.

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

Mostra come convertire documenti con una singola riga di codice usando il contesto.

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

Mostra come convertire documenti dallo stream con una singola riga di codice usando il contesto.

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

### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```


Specifica il documento di input per l'elaborazione.

 **Remarks:** 

Se il processore accetta solo un file come input, verrà elaborato solo l'ultimo file specificato. Il processore [Merger](../../com.aspose.words/merger/) accetta più file come input, quindi tutti i documenti specificati verranno uniti. Il processore [Converter](../../com.aspose.words/converter/) accetta solo un file come input, quindi solo l'ultimo file specificato verrà convertito.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | java.io.InputStream | Stream del documento di input. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Specifica il documento di input per l'elaborazione.

 **Remarks:** 

Se il processore accetta solo un file come input, verrà elaborato solo l'ultimo file specificato. Il processore [Merger](../../com.aspose.words/merger/) accetta più file come input, quindi tutti i documenti specificati verranno uniti. Il processore [Converter](../../com.aspose.words/converter/) accetta solo un file come input, quindi solo l'ultimo file specificato verrà convertito.

 **Examples:** 

Mostra come unire documenti dallo stream in un unico documento di output usando il contesto.

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

Mostra come convertire documenti dallo stream con una singola riga di codice usando il contesto.

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

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | java.io.InputStream | Stream del documento di input. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Opzioni di caricamento opzionali usate per caricare il documento. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Specifica il documento di input per l'elaborazione.

 **Remarks:** 

Se il processore accetta solo un file come input, verrà elaborato solo l'ultimo file specificato. Il processore [Merger](../../com.aspose.words/merger/) accetta più file come input, quindi tutti i documenti specificati verranno uniti. Il processore [Converter](../../com.aspose.words/converter/) accetta solo un file come input, quindi solo l'ultimo file specificato verrà convertito.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | java.lang.String | Nome file del documento di input. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Specifica il documento di input per l'elaborazione.

 **Remarks:** 

Se il processore accetta solo un file come input, verrà elaborato solo l'ultimo file specificato. Il processore [Merger](../../com.aspose.words/merger/) accetta più file come input, quindi tutti i documenti specificati verranno uniti. Il processore [Converter](../../com.aspose.words/converter/) accetta solo un file come input, quindi solo l'ultimo file specificato verrà convertito.

 **Examples:** 

Mostra come unire documenti in un unico documento di output usando il contesto.

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

Mostra come convertire documenti con una singola riga di codice usando il contesto.

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

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | java.lang.String | Nome file del documento di input. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Opzioni di caricamento opzionali usate per caricare il documento. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Specifica il file di output per il processore.

 **Remarks:** 

Se l'output consiste di più file, il nome file di output specificato viene usato per generare il nome file per ogni parte secondo la regola: 'outputFile\_partIndex.extension'.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.lang.String | Nome file di output. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Specifica il file di output per il processore.

 **Remarks:** 

Se l'output consiste di più file, il nome file di output specificato viene usato per generare il nome file per ogni parte secondo la regola: 'outputFile\_partIndex.extension'.

 **Examples:** 

Mostra come unire documenti in un unico documento di output usando il contesto.

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

Mostra come convertire documenti con una singola riga di codice usando il contesto.

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

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.lang.String | Nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Opzioni di salvataggio opzionali. Se non specificate, il formato di salvataggio è determinato dall'estensione del file. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
