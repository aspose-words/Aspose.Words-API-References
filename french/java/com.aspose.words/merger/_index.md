---
title: "Merger"
linktitle: "Merger"
second_title: "Aspose.Words pour Java"
description: "Représente un groupe de méthodes destinées à fusionner une variété de types de documents différents en un seul document de sortie en Java."
type: docs
weight: 465
url: /fr/java/com.aspose.words/merger/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Merger extends Processor
```

Représente un groupe de méthodes destinées à fusionner une variété de types de documents différents en un seul document de sortie.

 **Remarks:** 

Les fichiers ou flux d'entrée et de sortie spécifiés, ainsi que les options de fusion et d'enregistrement souhaitées, sont utilisés pour fusionner les documents d'entrée fournis en un seul document de sortie.

La fonctionnalité de fusion prend en charge plus de 35 formats de fichiers différents.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [create()](#create) | Crée une nouvelle instance du processeur de fusion de courrier. |
| [create(MergerContext context)](#create-com.aspose.words.MergerContext) | Crée une nouvelle instance du processeur de fusion de courrier. |
| [execute()](#execute) | Exécute l'action du processeur. |
| [from(InputStream input)](#from-java.io.InputStream) | Spécifie le document d'entrée pour le traitement. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Spécifie le document d'entrée pour le traitement. |
| [from(String input)](#from-java.lang.String) | Spécifie le document d'entrée pour le traitement. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Spécifie le document d'entrée pour le traitement. |
| [merge(Document[] inputDocuments, int mergeFormatMode)](#merge-com.aspose.words.Document---int) |  |
| [merge(InputStream[] inputStreams, LoadOptions[] loadOptions, int mergeFormatMode)](#merge-java.io.InputStream---com.aspose.words.LoadOptions---int) |  |
| [merge(InputStream[] inputStreams, int mergeFormatMode)](#merge-java.io.InputStream---int) |  |
| [merge(OutputStream outputStream, InputStream[] inputStreams, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int) |  |
| [merge(OutputStream outputStream, InputStream[] inputStreams, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.SaveOptions-int) |  |
| [merge(OutputStream outputStream, InputStream[] inputStreams, int saveFormat)](#merge-java.io.OutputStream-java.io.InputStream---int) |  |
| [merge(String outputFile, String[] inputFiles)](#merge-java.lang.String-java.lang.String) | Fusionne les documents d'entrée fournis en un seul document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés avec [MergeFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/mergeformatmode/\#KEEP-SOURCE-FORMATTING). |
| [merge(String outputFile, String[] inputFiles, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int) |  |
| [merge(String outputFile, String[] inputFiles, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---com.aspose.words.SaveOptions-int) |  |
| [merge(String outputFile, String[] inputFiles, int saveFormat, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---int-int) |  |
| [merge(String[] inputFiles, LoadOptions[] loadOptions, int mergeFormatMode)](#merge-java.lang.String---com.aspose.words.LoadOptions---int) |  |
| [merge(String[] inputFiles, int mergeFormatMode)](#merge-java.lang.String---int) |  |
| [mergeToImages(InputStream[] inputStreams, ImageSaveOptions saveOptions, int mergeFormatMode)](#mergeToImages-java.io.InputStream---com.aspose.words.ImageSaveOptions-int) |  |
| [mergeToImages(String[] inputFiles, ImageSaveOptions saveOptions, int mergeFormatMode)](#mergeToImages-java.lang.String---com.aspose.words.ImageSaveOptions-int) |  |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Spécifie le fichier de sortie pour le processeur. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Spécifie le fichier de sortie pour le processeur. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create() {#create}
```
public static Merger create()
```


Crée une nouvelle instance du processeur de fusion de courrier.

**Returns:**
[Merger](../../com.aspose.words/merger/)
### create(MergerContext context) {#create-com.aspose.words.MergerContext}
```
public static Merger create(MergerContext context)
```


Crée une nouvelle instance du processeur de fusion de courrier.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie en utilisant le contexte.

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

Montre comment fusionner des documents du flux en un seul document de sortie en utilisant le contexte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| context | [MergerContext](../../com.aspose.words/mergercontext/) |  |

**Returns:**
[Merger](../../com.aspose.words/merger/)
### execute() {#execute}
```
public void execute()
```


Exécute l'action du processeur.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie en utilisant le contexte.

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

Montre comment fusionner des documents du flux en un seul document de sortie en utilisant le contexte.

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

Montre comment convertir des documents avec une seule ligne de code en utilisant le contexte.

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

Montre comment convertir des documents du flux avec une seule ligne de code en utilisant le contexte.

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


Spécifie le document d'entrée pour le traitement.

 **Remarks:** 

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. Le processeur [Merger](../../com.aspose.words/merger/) accepte plusieurs fichiers en entrée, de sorte que tous les documents spécifiés seront fusionnés. Le processeur [Converter](../../com.aspose.words/converter/) n'accepte qu'un seul fichier en entrée, ainsi le dernier fichier spécifié sera converti.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| entrée | java.io.InputStream | Flux du document d'entrée. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Spécifie le document d'entrée pour le traitement.

 **Remarks:** 

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. Le processeur [Merger](../../com.aspose.words/merger/) accepte plusieurs fichiers en entrée, de sorte que tous les documents spécifiés seront fusionnés. Le processeur [Converter](../../com.aspose.words/converter/) n'accepte qu'un seul fichier en entrée, ainsi le dernier fichier spécifié sera converti.

 **Examples:** 

Montre comment fusionner des documents du flux en un seul document de sortie en utilisant le contexte.

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

Montre comment convertir des documents du flux avec une seule ligne de code en utilisant le contexte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| entrée | java.io.InputStream | Flux du document d'entrée. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Options de chargement facultatives utilisées pour charger le document. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Spécifie le document d'entrée pour le traitement.

 **Remarks:** 

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. Le processeur [Merger](../../com.aspose.words/merger/) accepte plusieurs fichiers en entrée, de sorte que tous les documents spécifiés seront fusionnés. Le processeur [Converter](../../com.aspose.words/converter/) n'accepte qu'un seul fichier en entrée, ainsi le dernier fichier spécifié sera converti.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| entrée | java.lang.String | Nom de fichier du document d'entrée. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Spécifie le document d'entrée pour le traitement.

 **Remarks:** 

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. Le processeur [Merger](../../com.aspose.words/merger/) accepte plusieurs fichiers en entrée, de sorte que tous les documents spécifiés seront fusionnés. Le processeur [Converter](../../com.aspose.words/converter/) n'accepte qu'un seul fichier en entrée, ainsi le dernier fichier spécifié sera converti.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie en utilisant le contexte.

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

Montre comment convertir des documents avec une seule ligne de code en utilisant le contexte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| entrée | java.lang.String | Nom de fichier du document d'entrée. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Options de chargement facultatives utilisées pour charger le document. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### merge(Document[] inputDocuments, int mergeFormatMode) {#merge-com.aspose.words.Document---int}
```
public static Document merge(Document[] inputDocuments, int mergeFormatMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| inputStreams | java.io.InputStream[] |  |
| saveFormat | int |  |

### merge(String outputFile, String[] inputFiles) {#merge-java.lang.String-java.lang.String}
```
public static void merge(String outputFile, String[] inputFiles)
```


Fusionne les documents d'entrée fournis en un seul document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés avec [MergeFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/mergeformatmode/\#KEEP-SOURCE-FORMATTING).

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| outputFile | java.lang.String | Le nom de fichier de sortie. |
| inputFiles | java.lang.String[] | Les noms de fichiers d'entrée. |

### merge(String outputFile, String[] inputFiles, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode) {#merge-java.lang.String-java.lang.String---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int}
```
public static void merge(String outputFile, String[] inputFiles, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Spécifie le fichier de sortie pour le processeur.

 **Remarks:** 

Si la sortie se compose de plusieurs fichiers, le nom de fichier de sortie spécifié est utilisé pour générer le nom de fichier de chaque partie selon la règle : 'outputFile\_partIndex.extension'.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.lang.String | Nom du fichier de sortie. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Spécifie le fichier de sortie pour le processeur.

 **Remarks:** 

Si la sortie se compose de plusieurs fichiers, le nom de fichier de sortie spécifié est utilisé pour générer le nom de fichier de chaque partie selon la règle : 'outputFile\_partIndex.extension'.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie en utilisant le contexte.

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

Montre comment convertir des documents avec une seule ligne de code en utilisant le contexte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.lang.String | Nom du fichier de sortie. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Options d'enregistrement facultatives. Si non spécifiées, le format d'enregistrement est déterminé par l'extension du fichier. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
