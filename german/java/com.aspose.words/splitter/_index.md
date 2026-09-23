---
title: "Splitter"
linktitle: "Splitter"
second_title: "Aspose.Words für Java"
description: "Stellt Methoden bereit, die dazu dienen, Dokumente in Teile zu splitten, wobei verschiedene Kriterien in Java verwendet werden."
type: docs
weight: 631
url: /de/java/com.aspose.words/splitter/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Splitter extends Processor
```

Stellt Methoden bereit, die dazu dienen, Dokumente anhand verschiedener Kriterien in Teile zu splitten.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [create(SplitterContext context)](#create-com.aspose.words.SplitterContext) | Erstellt eine neue Instanz des Splitter‑Prozessors. |
| [execute()](#execute) | Führt die Prozessor‑Aktion aus. |
| [extractPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, int startPageIndex, int pageCount)](#extractPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-int-int) |  |
| [extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount)](#extractPages-java.io.InputStream-java.io.OutputStream-int-int-int) |  |
| [extractPages(String inputFileName, String outputFileName, SaveOptions saveOptions, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-int-int) | Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten in einer neuen Datei unter Verwendung des angegebenen Speicherformats. |
| [extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-int-int) | Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten in einer neuen Datei. |
| [extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-int-int-int) |  |
| [from(InputStream input)](#from-java.io.InputStream) | Gibt das Eingabedokument für die Verarbeitung an. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Gibt das Eingabedokument für die Verarbeitung an. |
| [from(String input)](#from-java.lang.String) | Gibt das Eingabedokument für die Verarbeitung an. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Gibt das Eingabedokument für die Verarbeitung an. |
| [removeBlankPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)](#removeBlankPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat)](#removeBlankPages-java.io.InputStream-java.io.OutputStream-int) |  |
| [removeBlankPages(String inputFileName, String outputFileName)](#removeBlankPages-java.lang.String-java.lang.String) | Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe. |
| [removeBlankPages(String inputFileName, String outputFileName, SaveOptions saveOptions)](#removeBlankPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions) | Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe im angegebenen Format. |
| [removeBlankPages(String inputFileName, String outputFileName, int saveFormat)](#removeBlankPages-java.lang.String-java.lang.String-int) |  |
| [split(InputStream inputStream, SaveOptions saveOptions, SplitOptions options)](#split-java.io.InputStream-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions) | Teilt ein Dokument aus einem Eingabestream in mehrere Teile auf, basierend auf den angegebenen Split-Optionen, und gibt die resultierenden Teile als Array von Streams im angegebenen Speicherformat zurück. |
| [split(InputStream inputStream, int saveFormat, SplitOptions options)](#split-java.io.InputStream-int-com.aspose.words.SplitOptions) |  |
| [split(String inputFileName, String outputFileName, SaveOptions saveOptions, SplitOptions options)](#split-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions) | Teilt ein Dokument in mehrere Teile auf, basierend auf den angegebenen Split-Optionen, und speichert die resultierenden Teile in Dateien im angegebenen Speicherformat. |
| [split(String inputFileName, String outputFileName, SplitOptions options)](#split-java.lang.String-java.lang.String-com.aspose.words.SplitOptions) | Teilt ein Dokument in mehrere Teile auf, basierend auf den angegebenen Split-Optionen, und speichert die resultierenden Teile in Dateien. |
| [split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options)](#split-java.lang.String-java.lang.String-int-com.aspose.words.SplitOptions) |  |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Gibt die Ausgabedatei für den Prozessor an. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Gibt die Ausgabedatei für den Prozessor an. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(SplitterContext context) {#create-com.aspose.words.SplitterContext}
```
public static Splitter create(SplitterContext context)
```


Erstellt eine neue Instanz des Splitter‑Prozessors.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| context | [SplitterContext](../../com.aspose.words/splittercontext/) |  |

**Returns:**
[Splitter](../../com.aspose.words/splitter/)
### execute() {#execute}
```
public void execute()
```


Führt die Prozessor‑Aktion aus.

 **Examples:** 

Zeigt, wie man Dokumente zu einem einzigen Ausgabedokument im Kontext zusammenführt.

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

Zeigt, wie man Dokumente aus einem Stream zu einem einzigen Ausgabedokument im Kontext zusammenführt.

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

Zeigt, wie man Dokumente mit einer einzigen Codezeile im Kontext konvertiert.

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

Zeigt, wie man Dokumente aus einem Stream mit einer einzigen Codezeile im Kontext konvertiert.

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

### extractPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, int startPageIndex, int pageCount) {#extractPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-int-int}
```
public static void extractPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, int startPageIndex, int pageCount)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| startPageIndex | int |  |
| pageCount | int |  |

### extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount) {#extractPages-java.io.InputStream-java.io.OutputStream-int-int-int}
```
public static void extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| startPageIndex | int |  |
| pageCount | int |  |

### extractPages(String inputFileName, String outputFileName, SaveOptions saveOptions, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, SaveOptions saveOptions, int startPageIndex, int pageCount)
```


Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten in einer neuen Datei unter Verwendung des angegebenen Speicherformats.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen. |
| startPageIndex | int | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| pageCount | int | Anzahl der zu extrahierenden Seiten. |

### extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount)
```


Extrahiert einen angegebenen Seitenbereich aus einer Dokumentdatei und speichert die extrahierten Seiten in einer neuen Datei. Das Ausgabeformat wird anhand der Dateierweiterung des Ausgabedateinamens bestimmt.

 **Examples:** 

Zeigt, wie Seiten aus dem Dokument extrahiert werden.

```

 // There is a several ways to extract pages from the document:
 String doc = getMyDir() + "Big document.docx";

 Splitter.extractPages(doc, getArtifactsDir() + "LowCode.ExtractPages.1.docx", 0, 2);
 Splitter.extractPages(doc, getArtifactsDir() + "LowCode.ExtractPages.2.docx", SaveFormat.DOCX, 0, 2);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| startPageIndex | int | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| pageCount | int | Anzahl der zu extrahierenden Seiten. |

### extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-int-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| startPageIndex | int |  |
| pageCount | int |  |

### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```


Gibt das Eingabedokument für die Verarbeitung an.

 **Remarks:** 

Wenn der Prozessor nur eine Datei als Eingabe akzeptiert, wird nur die zuletzt angegebene Datei verarbeitet. Der [Merger](../../com.aspose.words/merger/) Prozessor akzeptiert mehrere Dateien als Eingabe, sodass alle angegebenen Dokumente zusammengeführt werden. Der [Converter](../../com.aspose.words/converter/) Prozessor akzeptiert nur eine Datei als Eingabe, daher wird nur die zuletzt angegebene Datei konvertiert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Eingabe | java.io.InputStream | Eingabedokumenten‑Stream. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Gibt das Eingabedokument für die Verarbeitung an.

 **Remarks:** 

Wenn der Prozessor nur eine Datei als Eingabe akzeptiert, wird nur die zuletzt angegebene Datei verarbeitet. Der [Merger](../../com.aspose.words/merger/) Prozessor akzeptiert mehrere Dateien als Eingabe, sodass alle angegebenen Dokumente zusammengeführt werden. Der [Converter](../../com.aspose.words/converter/) Prozessor akzeptiert nur eine Datei als Eingabe, daher wird nur die zuletzt angegebene Datei konvertiert.

 **Examples:** 

Zeigt, wie man Dokumente aus einem Stream zu einem einzigen Ausgabedokument im Kontext zusammenführt.

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

Zeigt, wie man Dokumente aus einem Stream mit einer einzigen Codezeile im Kontext konvertiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Eingabe | java.io.InputStream | Eingabedokumenten‑Stream. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Optionale Ladeoptionen, die zum Laden des Dokuments verwendet werden. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Gibt das Eingabedokument für die Verarbeitung an.

 **Remarks:** 

Wenn der Prozessor nur eine Datei als Eingabe akzeptiert, wird nur die zuletzt angegebene Datei verarbeitet. Der [Merger](../../com.aspose.words/merger/) Prozessor akzeptiert mehrere Dateien als Eingabe, sodass alle angegebenen Dokumente zusammengeführt werden. Der [Converter](../../com.aspose.words/converter/) Prozessor akzeptiert nur eine Datei als Eingabe, daher wird nur die zuletzt angegebene Datei konvertiert.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Eingabe | java.lang.String | Eingabedokumentdateiname. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Gibt das Eingabedokument für die Verarbeitung an.

 **Remarks:** 

Wenn der Prozessor nur eine Datei als Eingabe akzeptiert, wird nur die zuletzt angegebene Datei verarbeitet. Der [Merger](../../com.aspose.words/merger/) Prozessor akzeptiert mehrere Dateien als Eingabe, sodass alle angegebenen Dokumente zusammengeführt werden. Der [Converter](../../com.aspose.words/converter/) Prozessor akzeptiert nur eine Datei als Eingabe, daher wird nur die zuletzt angegebene Datei konvertiert.

 **Examples:** 

Zeigt, wie man Dokumente zu einem einzigen Ausgabedokument im Kontext zusammenführt.

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

Zeigt, wie man Dokumente mit einer einzigen Codezeile im Kontext konvertiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Eingabe | java.lang.String | Eingabedokumentdateiname. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Optionale Ladeoptionen, die zum Laden des Dokuments verwendet werden. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### removeBlankPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions) {#removeBlankPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public static ArrayList removeBlankPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
java.util.ArrayList
### removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat) {#removeBlankPages-java.io.InputStream-java.io.OutputStream-int}
```
public static ArrayList removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
java.util.ArrayList
### removeBlankPages(String inputFileName, String outputFileName) {#removeBlankPages-java.lang.String-java.lang.String}
```
public static ArrayList removeBlankPages(String inputFileName, String outputFileName)
```


Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe. Gibt eine Liste von Seitenzahlen zurück, die entfernt wurden.

 **Examples:** 

Zeigt, wie leere Seiten aus dem Dokument entfernt werden.

```

 // There is a several ways to remove empty pages from the document:
 String doc = getMyDir() + "Blank pages.docx";

 Splitter.removeBlankPages(doc, getArtifactsDir() + "LowCode.RemoveBlankPages.1.docx");
 Splitter.removeBlankPages(doc, getArtifactsDir() + "LowCode.RemoveBlankPages.2.docx", SaveFormat.DOCX);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |

**Returns:**
java.util.ArrayList – Liste von Seitenzahlen, die als leer betrachtet und entfernt wurden.
### removeBlankPages(String inputFileName, String outputFileName, SaveOptions saveOptions) {#removeBlankPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions}
```
public static ArrayList removeBlankPages(String inputFileName, String outputFileName, SaveOptions saveOptions)
```


Entfernt leere Seiten aus dem Dokument und speichert die Ausgabe im angegebenen Format. Gibt eine Liste von Seitenzahlen zurück, die entfernt wurden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen. |

**Returns:**
java.util.ArrayList – Liste von Seitenzahlen, die als leer betrachtet und entfernt wurden.
### removeBlankPages(String inputFileName, String outputFileName, int saveFormat) {#removeBlankPages-java.lang.String-java.lang.String-int}
```
public static ArrayList removeBlankPages(String inputFileName, String outputFileName, int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
java.util.ArrayList
### split(InputStream inputStream, SaveOptions saveOptions, SplitOptions options) {#split-java.io.InputStream-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions}
```
public static OutputStream[] split(InputStream inputStream, SaveOptions saveOptions, SplitOptions options)
```


Teilt ein Dokument aus einem Eingabestream in mehrere Teile auf, basierend auf den angegebenen Split-Optionen, und gibt die resultierenden Teile als Array von Streams im angegebenen Speicherformat zurück.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream | Der Eingabestream. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen. |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | Optionen zum Aufteilen des Dokuments. |

**Returns:**
java.io.OutputStream[]
### split(InputStream inputStream, int saveFormat, SplitOptions options) {#split-java.io.InputStream-int-com.aspose.words.SplitOptions}
```
public static OutputStream[] split(InputStream inputStream, int saveFormat, SplitOptions options)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveFormat | int |  |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) |  |

**Returns:**
java.io.OutputStream[]
### split(String inputFileName, String outputFileName, SaveOptions saveOptions, SplitOptions options) {#split-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, SaveOptions saveOptions, SplitOptions options)
```


Teilt ein Dokument in mehrere Teile auf, basierend auf den angegebenen Split-Optionen, und speichert die resultierenden Teile in Dateien im angegebenen Speicherformat.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname, der verwendet wird, um Dateinamen für Dokumentteile nach der Regel \"outputFile\\_partIndex.extension\" zu erzeugen. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen. |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | Optionen zum Aufteilen des Dokuments. |

### split(String inputFileName, String outputFileName, SplitOptions options) {#split-java.lang.String-java.lang.String-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, SplitOptions options)
```


Teilt ein Dokument in mehrere Teile auf, basierend auf den angegebenen Split-Optionen, und speichert die resultierenden Teile in Dateien. Das Ausgabeformat wird anhand der Dateierweiterung des Ausgabedateinamens bestimmt.

 **Examples:** 

Zeigt, wie das Dokument nach Seiten aufgeteilt wird.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String | Der Eingabedateiname. |
| outputFileName | java.lang.String | Der Ausgabedateiname, der verwendet wird, um Dateinamen für Dokumentteile nach der Regel \"outputFile\\_partIndex.extension\" zu erzeugen. |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | Optionen zum Aufteilen des Dokuments. |

### split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options) {#split-java.lang.String-java.lang.String-int-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) |  |

### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Gibt die Ausgabedatei für den Prozessor an.

 **Remarks:** 

Wenn die Ausgabe aus mehreren Dateien besteht, wird der angegebene Ausgabedateiname verwendet, um für jeden Teil gemäß der Regel 'outputFile\_partIndex.extension' einen Dateinamen zu erzeugen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.lang.String | Ausgabedateiname. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Gibt die Ausgabedatei für den Prozessor an.

 **Remarks:** 

Wenn die Ausgabe aus mehreren Dateien besteht, wird der angegebene Ausgabedateiname verwendet, um für jeden Teil gemäß der Regel 'outputFile\_partIndex.extension' einen Dateinamen zu erzeugen.

 **Examples:** 

Zeigt, wie man Dokumente zu einem einzigen Ausgabedokument im Kontext zusammenführt.

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

Zeigt, wie man Dokumente mit einer einzigen Codezeile im Kontext konvertiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.lang.String | Ausgabedateiname. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Optionale Speicheroptionen. Wenn nicht angegeben, wird das Speicherformat anhand der Dateierweiterung bestimmt. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ausgabe | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
