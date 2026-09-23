---
title: "Merger"
linktitle: "Merger"
second_title: "Aspose.Words für Java"
description: "Stellt eine Gruppe von Methoden dar, die dazu bestimmt sind, verschiedene Dokumenttypen in einem einzigen Ausgabedokument in Java zusammenzuführen."
type: docs
weight: 465
url: /de/java/com.aspose.words/merger/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Merger extends Processor
```

Stellt eine Gruppe von Methoden dar, die dazu dienen, verschiedene Dokumenttypen zu einem einzigen Ausgabedokument zusammenzuführen.

 **Remarks:** 

Die angegebenen Eingabe- und Ausgabedateien oder -streams sowie die gewünschten Zusammenführungs- und Speicheroptionen werden verwendet, um die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammenzuführen.

Die Zusammenführungsfunktion unterstützt über 35 verschiedene Dateiformate.

 **Examples:** 

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.1.docx", new String[]{inputDoc1, inputDoc2});

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.2.docx", new String[]{inputDoc1, inputDoc2}, saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.3.pdf", new String[]{inputDoc1, inputDoc2}, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.4.docx", new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions},
         saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Document doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.5.docx");

 doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.6.docx");
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [create()](#create) | Erstellt eine neue Instanz des MailMerger‑Processors. |
| [create(MergerContext context)](#create-com.aspose.words.MergerContext) | Erstellt eine neue Instanz des MailMerger‑Processors. |
| [execute()](#execute) | Führt die Prozessor‑Aktion aus. |
| [from(InputStream input)](#from-java.io.InputStream) | Gibt das Eingabedokument für die Verarbeitung an. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Gibt das Eingabedokument für die Verarbeitung an. |
| [from(String input)](#from-java.lang.String) | Gibt das Eingabedokument für die Verarbeitung an. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Gibt das Eingabedokument für die Verarbeitung an. |
| [merge(Document[] inputDocuments, int mergeFormatMode)](#merge-com.aspose.words.Document---int) |  |
| [merge(InputStream[] inputStreams, LoadOptions[] loadOptions, int mergeFormatMode)](#merge-java.io.InputStream---com.aspose.words.LoadOptions---int) |  |
| [merge(InputStream[] inputStreams, int mergeFormatMode)](#merge-java.io.InputStream---int) |  |
| [merge(OutputStream outputStream, InputStream[] inputStreams, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int) |  |
| [merge(OutputStream outputStream, InputStream[] inputStreams, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.SaveOptions-int) |  |
| [merge(OutputStream outputStream, InputStream[] inputStreams, int saveFormat)](#merge-java.io.OutputStream-java.io.InputStream---int) |  |
| [merge(String outputFile, String[] inputFiles)](#merge-java.lang.String-java.lang.String) | Führt die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammen, indem die angegebenen Eingabe- und Ausgabedateinamen verwendet werden, unter Verwendung von [MergeFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/mergeformatmode/\#KEEP-SOURCE-FORMATTING). |
| [merge(String outputFile, String[] inputFiles, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int) |  |
| [merge(String outputFile, String[] inputFiles, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---com.aspose.words.SaveOptions-int) |  |
| [merge(String outputFile, String[] inputFiles, int saveFormat, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---int-int) |  |
| [merge(String[] inputFiles, LoadOptions[] loadOptions, int mergeFormatMode)](#merge-java.lang.String---com.aspose.words.LoadOptions---int) |  |
| [merge(String[] inputFiles, int mergeFormatMode)](#merge-java.lang.String---int) |  |
| [mergeToImages(InputStream[] inputStreams, ImageSaveOptions saveOptions, int mergeFormatMode)](#mergeToImages-java.io.InputStream---com.aspose.words.ImageSaveOptions-int) |  |
| [mergeToImages(String[] inputFiles, ImageSaveOptions saveOptions, int mergeFormatMode)](#mergeToImages-java.lang.String---com.aspose.words.ImageSaveOptions-int) |  |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Gibt die Ausgabedatei für den Prozessor an. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Gibt die Ausgabedatei für den Prozessor an. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create() {#create}
```
public static Merger create()
```


Erstellt eine neue Instanz des MailMerger‑Processors.

**Returns:**
[Merger](../../com.aspose.words/merger/)
### create(MergerContext context) {#create-com.aspose.words.MergerContext}
```
public static Merger create(MergerContext context)
```


Erstellt eine neue Instanz des MailMerger‑Processors.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| context | [MergerContext](../../com.aspose.words/mergercontext/) |  |

**Returns:**
[Merger](../../com.aspose.words/merger/)
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
### merge(Document[] inputDocuments, int mergeFormatMode) {#merge-com.aspose.words.Document---int}
```
public static Document merge(Document[] inputDocuments, int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputDocuments | [Document\[\]](../../com.aspose.words/document/) |  |
| mergeFormatMode | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### merge(InputStream[] inputStreams, LoadOptions[] loadOptions, int mergeFormatMode) {#merge-java.io.InputStream---com.aspose.words.LoadOptions---int}
```
public static Document merge(InputStream[] inputStreams, LoadOptions[] loadOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStreams | java.io.InputStream[] |  |
| loadOptions | [LoadOptions\[\]](../../com.aspose.words/loadoptions/) |  |
| mergeFormatMode | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### merge(InputStream[] inputStreams, int mergeFormatMode) {#merge-java.io.InputStream---int}
```
public static Document merge(InputStream[] inputStreams, int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStreams | java.io.InputStream[] |  |
| mergeFormatMode | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### merge(OutputStream outputStream, InputStream[] inputStreams, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode) {#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int}
```
public static void merge(OutputStream outputStream, InputStream[] inputStreams, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| inputStreams | java.io.InputStream[] |  |
| loadOptions | [LoadOptions\[\]](../../com.aspose.words/loadoptions/) |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mergeFormatMode | int |  |

### merge(OutputStream outputStream, InputStream[] inputStreams, SaveOptions saveOptions, int mergeFormatMode) {#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.SaveOptions-int}
```
public static void merge(OutputStream outputStream, InputStream[] inputStreams, SaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| inputStreams | java.io.InputStream[] |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mergeFormatMode | int |  |

### merge(OutputStream outputStream, InputStream[] inputStreams, int saveFormat) {#merge-java.io.OutputStream-java.io.InputStream---int}
```
public static void merge(OutputStream outputStream, InputStream[] inputStreams, int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| inputStreams | java.io.InputStream[] |  |
| saveFormat | int |  |

### merge(String outputFile, String[] inputFiles) {#merge-java.lang.String-java.lang.String}
```
public static void merge(String outputFile, String[] inputFiles)
```


Führt die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammen, indem die angegebenen Eingabe- und Ausgabedateinamen verwendet werden, unter Verwendung von [MergeFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/mergeformatmode/\#KEEP-SOURCE-FORMATTING).

 **Remarks:** 

Wenn das Ausgabeformat ein Bild (BMP, EMF, EPS, GIF, JPEG, PNG oder WebP) ist, wird jede Seite der Ausgabe als separate Datei gespeichert. Der angegebene Ausgabedateiname wird verwendet, um Dateinamen für jeden Teil nach der Regel zu erzeugen: outputFile\_partIndex.extension.

Wenn das Ausgabeformat TIFF ist, wird die Ausgabe als einzelne mehrseitige TIFF-Datei gespeichert.

 **Examples:** 

Zeigt, wie Dokumente zu einem einzigen Ausgabedokument zusammengeführt werden.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.1.docx", new String[]{inputDoc1, inputDoc2});

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.2.docx", new String[]{inputDoc1, inputDoc2}, saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.3.pdf", new String[]{inputDoc1, inputDoc2}, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.4.docx", new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions},
         saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Document doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.5.docx");

 doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.6.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputFile | java.lang.String | Der Ausgabedateiname. |
| inputFiles | java.lang.String[] | Die Eingabedateinamen. |

### merge(String outputFile, String[] inputFiles, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode) {#merge-java.lang.String-java.lang.String---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int}
```
public static void merge(String outputFile, String[] inputFiles, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputFile | java.lang.String |  |
| inputFiles | java.lang.String[] |  |
| loadOptions | [LoadOptions\[\]](../../com.aspose.words/loadoptions/) |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mergeFormatMode | int |  |

### merge(String outputFile, String[] inputFiles, SaveOptions saveOptions, int mergeFormatMode) {#merge-java.lang.String-java.lang.String---com.aspose.words.SaveOptions-int}
```
public static void merge(String outputFile, String[] inputFiles, SaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputFile | java.lang.String |  |
| inputFiles | java.lang.String[] |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| mergeFormatMode | int |  |

### merge(String outputFile, String[] inputFiles, int saveFormat, int mergeFormatMode) {#merge-java.lang.String-java.lang.String---int-int}
```
public static void merge(String outputFile, String[] inputFiles, int saveFormat, int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputFile | java.lang.String |  |
| inputFiles | java.lang.String[] |  |
| saveFormat | int |  |
| mergeFormatMode | int |  |

### merge(String[] inputFiles, LoadOptions[] loadOptions, int mergeFormatMode) {#merge-java.lang.String---com.aspose.words.LoadOptions---int}
```
public static Document merge(String[] inputFiles, LoadOptions[] loadOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFiles | java.lang.String[] |  |
| loadOptions | [LoadOptions\[\]](../../com.aspose.words/loadoptions/) |  |
| mergeFormatMode | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### merge(String[] inputFiles, int mergeFormatMode) {#merge-java.lang.String---int}
```
public static Document merge(String[] inputFiles, int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFiles | java.lang.String[] |  |
| mergeFormatMode | int |  |

**Returns:**
[Document](../../com.aspose.words/document/)
### mergeToImages(InputStream[] inputStreams, ImageSaveOptions saveOptions, int mergeFormatMode) {#mergeToImages-java.io.InputStream---com.aspose.words.ImageSaveOptions-int}
```
public static InputStream[] mergeToImages(InputStream[] inputStreams, ImageSaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStreams | java.io.InputStream[] |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| mergeFormatMode | int |  |

**Returns:**
java.io.InputStream[]
### mergeToImages(String[] inputFiles, ImageSaveOptions saveOptions, int mergeFormatMode) {#mergeToImages-java.lang.String---com.aspose.words.ImageSaveOptions-int}
```
public static InputStream[] mergeToImages(String[] inputFiles, ImageSaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFiles | java.lang.String[] |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |
| mergeFormatMode | int |  |

**Returns:**
java.io.InputStream[]
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
