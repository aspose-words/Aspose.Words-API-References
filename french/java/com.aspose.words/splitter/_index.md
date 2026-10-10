---
title: "Splitter"
linktitle: "Splitter"
second_title: "Aspose.Words pour Java"
description: "Fournit des méthodes destinées à diviser les documents en parties selon différents critères en Java."
type: docs
weight: 631
url: /fr/java/com.aspose.words/splitter/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Splitter extends Processor
```

Fournit des méthodes destinées à découper les documents en parties en utilisant différents critères.
## Méthodes

| Méthode | Description |
| --- | --- |
| [create(SplitterContext context)](#create-com.aspose.words.SplitterContext) | Crée une nouvelle instance du processeur de division. |
| [execute()](#execute) | Exécute l'action du processeur. |
| [extractPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, int startPageIndex, int pageCount)](#extractPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-int-int) |  |
| [extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount)](#extractPages-java.io.InputStream-java.io.OutputStream-int-int-int) |  |
| [extractPages(String inputFileName, String outputFileName, SaveOptions saveOptions, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-int-int) | Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier en utilisant le format d'enregistrement spécifié. |
| [extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-int-int) | Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier. |
| [extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-int-int-int) |  |
| [from(InputStream input)](#from-java.io.InputStream) | Spécifie le document d'entrée pour le traitement. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Spécifie le document d'entrée pour le traitement. |
| [from(String input)](#from-java.lang.String) | Spécifie le document d'entrée pour le traitement. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Spécifie le document d'entrée pour le traitement. |
| [removeBlankPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)](#removeBlankPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat)](#removeBlankPages-java.io.InputStream-java.io.OutputStream-int) |  |
| [removeBlankPages(String inputFileName, String outputFileName)](#removeBlankPages-java.lang.String-java.lang.String) | Supprime les pages vides du document et enregistre la sortie. |
| [removeBlankPages(String inputFileName, String outputFileName, SaveOptions saveOptions)](#removeBlankPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions) | Supprime les pages vides du document et enregistre la sortie au format spécifié. |
| [removeBlankPages(String inputFileName, String outputFileName, int saveFormat)](#removeBlankPages-java.lang.String-java.lang.String-int) |  |
| [split(InputStream inputStream, SaveOptions saveOptions, SplitOptions options)](#split-java.io.InputStream-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions) | Divise un document à partir d'un flux d'entrée en plusieurs parties en fonction des options de division spécifiées et renvoie les parties résultantes sous forme de tableau de flux au format d'enregistrement spécifié. |
| [split(InputStream inputStream, int saveFormat, SplitOptions options)](#split-java.io.InputStream-int-com.aspose.words.SplitOptions) |  |
| [split(String inputFileName, String outputFileName, SaveOptions saveOptions, SplitOptions options)](#split-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-com.aspose.words.SplitOptions) | Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers au format d'enregistrement spécifié. |
| [split(String inputFileName, String outputFileName, SplitOptions options)](#split-java.lang.String-java.lang.String-com.aspose.words.SplitOptions) | Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers. |
| [split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options)](#split-java.lang.String-java.lang.String-int-com.aspose.words.SplitOptions) |  |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Spécifie le fichier de sortie pour le processeur. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Spécifie le fichier de sortie pour le processeur. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(SplitterContext context) {#create-com.aspose.words.SplitterContext}
```
public static Splitter create(SplitterContext context)
```


Crée une nouvelle instance du processeur de division.

 **Examples:** 

Montre comment diviser le document par pages en utilisant le contexte.

```

 String doc = getMyDir() + "Big document.docx";

 SplitterContext splitterContext = new SplitterContext();
 splitterContext.getSplitOptions().setSplitCriteria(SplitCriteria.PAGE);

 Splitter.create(splitterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.SplitContextDocument.docx")
         .execute();
 
```

Montre comment diviser le document depuis le flux par pages en utilisant le contexte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| context | [SplitterContext](../../com.aspose.words/splittercontext/) |  |

**Returns:**
[Splitter](../../com.aspose.words/splitter/)
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

### extractPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, int startPageIndex, int pageCount) {#extractPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-int-int}
```
public static void extractPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, int startPageIndex, int pageCount)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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


Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier en utilisant le format d'enregistrement spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Les options d'enregistrement. |
| startPageIndex | int | L'indice basé sur zéro de la première page à extraire. |
| pageCount | int | Nombre de pages à extraire. |

### extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount)
```


Extrait une plage de pages spécifiée d'un fichier de document et enregistre les pages extraites dans un nouveau fichier. Le format du fichier de sortie est déterminé par l'extension du nom du fichier de sortie.

 **Examples:** 

Montre comment extraire des pages du document.

```

 // There is a several ways to extract pages from the document:
 String doc = getMyDir() + "Big document.docx";

 Splitter.extractPages(doc, getArtifactsDir() + "LowCode.ExtractPages.1.docx", 0, 2);
 Splitter.extractPages(doc, getArtifactsDir() + "LowCode.ExtractPages.2.docx", SaveFormat.DOCX, 0, 2);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| startPageIndex | int | L'indice basé sur zéro de la première page à extraire. |
| pageCount | int | Nombre de pages à extraire. |

### extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-int-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount)
```




**Parameters:**
| Paramètre | Type | Description |
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
### removeBlankPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions) {#removeBlankPages-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public static ArrayList removeBlankPages(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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


Supprime les pages vides du document et enregistre la sortie. Retourne une liste des numéros de pages qui ont été supprimés.

 **Examples:** 

Montre comment supprimer les pages vides du document.

```

 // There is a several ways to remove empty pages from the document:
 String doc = getMyDir() + "Blank pages.docx";

 Splitter.removeBlankPages(doc, getArtifactsDir() + "LowCode.RemoveBlankPages.1.docx");
 Splitter.removeBlankPages(doc, getArtifactsDir() + "LowCode.RemoveBlankPages.2.docx", SaveFormat.DOCX);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |

**Returns:**
java.util.ArrayList - La liste des numéros de pages a été considérée comme vide et supprimée.
### removeBlankPages(String inputFileName, String outputFileName, SaveOptions saveOptions) {#removeBlankPages-java.lang.String-java.lang.String-com.aspose.words.SaveOptions}
```
public static ArrayList removeBlankPages(String inputFileName, String outputFileName, SaveOptions saveOptions)
```


Supprime les pages vides du document et enregistre la sortie au format spécifié. Retourne une liste des numéros de pages qui ont été supprimés.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Les options d'enregistrement. |

**Returns:**
java.util.ArrayList - La liste des numéros de pages a été considérée comme vide et supprimée.
### removeBlankPages(String inputFileName, String outputFileName, int saveFormat) {#removeBlankPages-java.lang.String-java.lang.String-int}
```
public static ArrayList removeBlankPages(String inputFileName, String outputFileName, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
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


Divise un document à partir d'un flux d'entrée en plusieurs parties en fonction des options de division spécifiées et renvoie les parties résultantes sous forme de tableau de flux au format d'enregistrement spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | Le flux d'entrée. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Les options d'enregistrement. |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | Options de division du document. |

**Returns:**
java.io.OutputStream[]
### split(InputStream inputStream, int saveFormat, SplitOptions options) {#split-java.io.InputStream-int-com.aspose.words.SplitOptions}
```
public static OutputStream[] split(InputStream inputStream, int saveFormat, SplitOptions options)
```




**Parameters:**
| Paramètre | Type | Description |
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


Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers au format d'enregistrement spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom du fichier de sortie utilisé pour générer le nom de fichier des parties du document en utilisant la règle "outputFile\_partIndex.extension" |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Les options d'enregistrement. |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | Options de division du document. |

### split(String inputFileName, String outputFileName, SplitOptions options) {#split-java.lang.String-java.lang.String-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, SplitOptions options)
```


Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers. Le format du fichier de sortie est déterminé par l'extension du nom du fichier de sortie.

 **Examples:** 

Montre comment diviser le document par pages.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom du fichier de sortie utilisé pour générer le nom de fichier des parties du document en utilisant la règle "outputFile\_partIndex.extension" |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | Options de division du document. |

### split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options) {#split-java.lang.String-java.lang.String-int-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options)
```




**Parameters:**
| Paramètre | Type | Description |
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
