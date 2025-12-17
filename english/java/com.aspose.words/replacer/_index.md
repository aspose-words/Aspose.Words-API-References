---
title: Replacer
linktitle: Replacer
second_title: Aspose.Words for Java
description: Provides methods intended to find and replace text in the document in Java.
type: docs
weight: 564
url: /java/com.aspose.words/replacer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Replacer extends Processor
```

Provides methods intended to find and replace text in the document.
## Methods

| Method | Description |
| --- | --- |
| [create(ReplacerContext context)](#create-com.aspose.words.ReplacerContext) | Creates new instance of the replacer processor. |
| [execute()](#execute) | Execute the processor action. |
| [from(InputStream input)](#from-java.io.InputStream) | Specifies input document for processing. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Specifies input document for processing. |
| [from(String input)](#from-java.lang.String) | Specifies input document for processing. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Specifies input document for processing. |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file, with the specified save format and additional options. |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file, with the specified save format and additional options. |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression, with the specified save format and additional options. |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression, with the specified save format and additional options. |
| [replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-java.lang.String-java.lang.String) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file. |
| [replace(String inputFileName, String outputFileName, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-java.util.regex.Pattern-java.lang.String) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String) | Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | Replaces all occurrences of a specified character string pattern with a replacement string in the input file. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String) | Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Specifies output file for the processor. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Specifies output file for the processor. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(ReplacerContext context) {#create-com.aspose.words.ReplacerContext}
```
public static Replacer create(ReplacerContext context)
```


Creates new instance of the replacer processor.

 **Examples:** 

Shows how to replace string with regex in the document using context.

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

Shows how to replace string in the document using context.

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

Shows how to replace string with regex in the document using documents from the stream using context.

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

Shows how to replace string in the document using documents from the stream using context.

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
| Parameter | Type | Description |
| --- | --- | --- |
| context | [ReplacerContext](../../com.aspose.words/replacercontext/) |  |

**Returns:**
[Replacer](../../com.aspose.words/replacer/)
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


Specifies input document for processing.

 **Remarks:** 

If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../com.aspose.words/merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../com.aspose.words/converter/) processor accepts only one file as an input, so only the last specified file will be converted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.io.InputStream | Input document stream. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
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


Specifies input document for processing.

 **Remarks:** 

If the processor accepts only one file as an input, only the last specified file will be processed. [Merger](../../com.aspose.words/merger/) processor accepts multiple files as an input, as the result all the specified documents will be merged. [Converter](../../com.aspose.words/converter/) processor accepts only one file as an input, so only the last specified file will be converted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| input | java.lang.String | Input document file name. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
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
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| pattern | java.lang.String |  |
| replacement | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| pattern | java.lang.String |  |
| replacement | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| pattern | java.util.regex.Pattern |  |
| replacement | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| pattern | java.util.regex.Pattern |  |
| replacement | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| pattern | java.lang.String |  |
| replacement | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| pattern | java.lang.String |  |
| replacement | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| pattern | java.util.regex.Pattern |  |
| replacement | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| pattern | java.util.regex.Pattern |  |
| replacement | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement)
```


Replaces all occurrences of a specified character string pattern with a replacement string in the input file, with the specified save format and additional options.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The save options. |
| pattern | java.lang.String | A string to be replaced. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |

**Returns:**
int - The number of replacements made.
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


Replaces all occurrences of a specified character string pattern with a replacement string in the input file, with the specified save format and additional options.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The save options. |
| pattern | java.lang.String | A string to be replaced. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) object to specify additional options. |

**Returns:**
int - The number of replacements made.
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement)
```


Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression, with the specified save format and additional options.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The save options. |
| pattern | java.util.regex.Pattern | A regular expression pattern used to find matches. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |

**Returns:**
int - The number of replacements made.
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression, with the specified save format and additional options.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The save options. |
| pattern | java.util.regex.Pattern | A regular expression pattern used to find matches. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) object to specify additional options. |

**Returns:**
int - The number of replacements made.
### replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| pattern | java.lang.String |  |
| replacement | java.lang.String |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| pattern | java.lang.String |  |
| replacement | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| pattern | java.util.regex.Pattern |  |
| replacement | java.lang.String |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| pattern | java.util.regex.Pattern |  |
| replacement | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, String pattern, String replacement)
```


Replaces all occurrences of a specified character string pattern with a replacement string in the input file.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to replace string in the document.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.Replace.1.docx", pattern, replacement);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.Replace.2.docx", SaveFormat.DOCX, pattern, replacement);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.Replace.3.docx", SaveFormat.DOCX, pattern, replacement, options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| pattern | java.lang.String | A string to be replaced. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |

**Returns:**
int - The number of replacements made.
### replace(String inputFileName, String outputFileName, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, Pattern pattern, String replacement)
```


Replaces all occurrences of a specified character string pattern with a replacement string in the input file using a regular expression.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to replace string with regex in the document.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "gr(a|e)y";
 String replacement = "lavender";

 Replacer.replace(doc, getArtifactsDir() + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.ReplaceRegex.2.docx", SaveFormat.DOCX, pattern, replacement);
 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.ReplaceRegex.3.docx", SaveFormat.DOCX, pattern, replacement, options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| pattern | java.util.regex.Pattern | A regular expression pattern used to find matches. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |

**Returns:**
int - The number of replacements made.
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement)
```


Replaces all occurrences of a specified character string pattern with a replacement string in the input file. Renders output to images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input file stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The save options. |
| pattern | java.lang.String | A string to be replaced. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


Replaces all occurrences of a specified character string pattern with a replacement string in the input file. Renders output to images.

 **Examples:** 

Shows how to replace string in the document using documents from the stream and save result to images.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     OutputStream[] images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);

     FindReplaceOptions options = new FindReplaceOptions();
     options.setFindWholeWordsOnly(false);
     images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input file stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The save options. |
| pattern | java.lang.String | A string to be replaced. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) object to specify additional options. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement)
```


Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. Renders output to images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input file stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The save options. |
| pattern | java.util.regex.Pattern | A regular expression pattern used to find matches. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. Renders output to images.

 **Examples:** 

Shows how to replace string with regex in the document using documents from the stream and save result to images.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     OutputStream[] images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);
     FindReplaceOptions options = new FindReplaceOptions();
     options.setFindWholeWordsOnly(false);
     images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input file stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The save options. |
| pattern | java.util.regex.Pattern | A regular expression pattern used to find matches. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) object to specify additional options. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement)
```


Replaces all occurrences of a specified character string pattern with a replacement string in the input file. Renders output to images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The save options. |
| pattern | java.lang.String | A string to be replaced. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


Replaces all occurrences of a specified character string pattern with a replacement string in the input file. Renders output to images.

 **Examples:** 

Shows how to replace string in the document and save result to images.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 OutputStream[] images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);

 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The save options. |
| pattern | java.lang.String | A string to be replaced. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) object to specify additional options. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement)
```


Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. Renders output to images.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The save options. |
| pattern | java.util.regex.Pattern | A regular expression pattern used to find matches. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


Replaces all occurrences of a specified regular expression pattern with a replacement string in the input file. Renders output to images.

 **Examples:** 

Shows how to replace string with regex in the document and save result to images.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 OutputStream[] images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);
 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | The save options. |
| pattern | java.util.regex.Pattern | A regular expression pattern used to find matches. |
| replacement | java.lang.String | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) object to specify additional options. |

**Returns:**
java.io.OutputStream[]
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


Specifies output file for the processor.

 **Remarks:** 

If the output consists of multiple files, the specified output file name is used to generate the file name for each part following the rule: 'outputFile\_partIndex.extension'.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| output | java.lang.String | Output file name. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
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
