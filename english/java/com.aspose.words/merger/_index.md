---
title: Merger
linktitle: Merger
second_title: Aspose.Words for Java
description: Represents a group of methods intended to merge a variety of different types of documents into a single output document in Java.
type: docs
weight: 463
url: /java/com.aspose.words/merger/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Merger extends Processor
```

Represents a group of methods intended to merge a variety of different types of documents into a single output document.

 **Remarks:** 

The specified input and output files or streams, along with the desired merge and save options, are used to merge the given input documents into a single output document.

The merging functionality supports over 35 different file formats.

 **Examples:** 

Shows how to merge documents into a single output document.

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
## Methods

| Method | Description |
| --- | --- |
| [create()](#create) | Creates new instance of the mail merger processor. |
| [create(MergerContext context)](#create-com.aspose.words.MergerContext) | Creates new instance of the mail merger processor. |
| [execute()](#execute) | Execute the processor action. |
| [from(InputStream input)](#from-java.io.InputStream) |  |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Specifies input document for processing. |
| [from(String input)](#from-java.lang.String) |  |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Specifies input document for processing. |
| [merge(Document[] inputDocuments, int mergeFormatMode)](#merge-com.aspose.words.Document---int) |  |
| [merge(InputStream[] inputStreams, LoadOptions[] loadOptions, int mergeFormatMode)](#merge-java.io.InputStream---com.aspose.words.LoadOptions---int) |  |
| [merge(InputStream[] inputStreams, int mergeFormatMode)](#merge-java.io.InputStream---int) |  |
| [merge(OutputStream outputStream, InputStream[] inputStreams, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int) |  |
| [merge(OutputStream outputStream, InputStream[] inputStreams, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.SaveOptions-int) |  |
| [merge(OutputStream outputStream, InputStream[] inputStreams, int saveFormat)](#merge-java.io.OutputStream-java.io.InputStream---int) |  |
| [merge(String outputFile, String[] inputFiles)](#merge-java.lang.String-java.lang.String) | Merges the given input documents into a single output document using specified input and output file names using [MergeFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/mergeformatmode/\#KEEP-SOURCE-FORMATTING). |
| [merge(String outputFile, String[] inputFiles, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int) |  |
| [merge(String outputFile, String[] inputFiles, SaveOptions saveOptions, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---com.aspose.words.SaveOptions-int) |  |
| [merge(String outputFile, String[] inputFiles, int saveFormat, int mergeFormatMode)](#merge-java.lang.String-java.lang.String---int-int) |  |
| [merge(String[] inputFiles, LoadOptions[] loadOptions, int mergeFormatMode)](#merge-java.lang.String---com.aspose.words.LoadOptions---int) |  |
| [merge(String[] inputFiles, int mergeFormatMode)](#merge-java.lang.String---int) |  |
| [mergeToImages(InputStream[] inputStreams, ImageSaveOptions saveOptions, int mergeFormatMode)](#mergeToImages-java.io.InputStream---com.aspose.words.ImageSaveOptions-int) |  |
| [mergeToImages(String[] inputFiles, ImageSaveOptions saveOptions, int mergeFormatMode)](#mergeToImages-java.lang.String---com.aspose.words.ImageSaveOptions-int) |  |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) |  |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Specifies output file for the processor. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create() {#create}
```
public static Merger create()
```


Creates new instance of the mail merger processor.

**Returns:**
[Merger](../../com.aspose.words/merger/)
### create(MergerContext context) {#create-com.aspose.words.MergerContext}
```
public static Merger create(MergerContext context)
```


Creates new instance of the mail merger processor.

 **Examples:** 

Shows how to merge documents into a single output document using context.

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

Shows how to merge documents from stream into a single output document using context.

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
| Parameter | Type | Description |
| --- | --- | --- |
| context | [MergerContext](../../com.aspose.words/mergercontext/) |  |

**Returns:**
[Merger](../../com.aspose.words/merger/)
### execute() {#execute}
```
public void execute()
```


Execute the processor action.

 **Examples:** 

Shows how to convert documents with a single line of code using context.

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

Shows how to convert documents from a stream with a single line of code using context.

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

Shows how to merge documents into a single output document using context.

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

Shows how to merge documents from stream into a single output document using context.

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

### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.io.InputStream |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Specifies input document for processing.

 **Remarks:** 

If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../com.aspose.words/merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../com.aspose.words/converter/) processor accepts only one file as an input, so only the last specified file will be converted.

 **Examples:** 

Shows how to convert documents from a stream with a single line of code using context.

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

Shows how to merge documents from stream into a single output document using context.

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
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.io.InputStream | Input document stream. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Optional load options used to load the document. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.lang.String |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Specifies input document for processing.

 **Remarks:** 

If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../com.aspose.words/merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../com.aspose.words/converter/) processor accepts only one file as an input, so only the last specified file will be converted.

 **Examples:** 

Shows how to convert documents with a single line of code using context.

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

Shows how to merge documents into a single output document using context.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.lang.String | Input document file name. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Optional load options used to load the document. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### merge(Document[] inputDocuments, int mergeFormatMode) {#merge-com.aspose.words.Document---int}
```
public static Document merge(Document[] inputDocuments, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| inputStreams | java.io.InputStream[] |  |
| saveFormat | int |  |

### merge(String outputFile, String[] inputFiles) {#merge-java.lang.String-java.lang.String}
```
public static void merge(String outputFile, String[] inputFiles)
```


Merges the given input documents into a single output document using specified input and output file names using [MergeFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/mergeformatmode/\#KEEP-SOURCE-FORMATTING).

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to merge documents into a single output document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| outputFile | java.lang.String | The output file name. |
| inputFiles | java.lang.String[] | The input file names. |

### merge(String outputFile, String[] inputFiles, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode) {#merge-java.lang.String-java.lang.String---com.aspose.words.LoadOptions---com.aspose.words.SaveOptions-int}
```
public static void merge(String outputFile, String[] inputFiles, LoadOptions[] loadOptions, SaveOptions saveOptions, int mergeFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.lang.String |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Specifies output file for the processor.

 **Remarks:** 

If the output consists of multiple files, the specified output file name is used to generate the file name for each part following the rule: 'outputFile\_partIndex.extension'.

 **Examples:** 

Shows how to convert documents with a single line of code using context.

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

Shows how to merge documents into a single output document using context.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.lang.String | Output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Optional save options. If not specified, save format is determined by the file extension. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
