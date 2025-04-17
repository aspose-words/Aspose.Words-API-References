---
title: Converter
linktitle: Converter
second_title: Aspose.Words for Java
description: Represents a group of methods intended to convert a variety of different types of documents using a single line of code in Java.
type: docs
weight: 131
url: /java/com.aspose.words/converter/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Converter extends Processor
```

Represents a group of methods intended to convert a variety of different types of documents using a single line of code.

 **Remarks:** 

The specified input and output files or streams, along with the desired save format, are used to convert the given input document of the one format into the output document of the other specified format.

The convert functionality supports over 35+ different file formats.

The **M:Aspose.Words.LowCode.Converter.ConvertToImages(System.String,Aspose.Words.SaveFormat)** group of methods are designed to transform documents into images, with each page being converted into a separate image file. These methods also convert PDF documents directly to fixed-page formats without loading them into the document model, which enhances both performance and accuracy.

With [ImageSaveOptions.getPageSet()](../../com.aspose.words/imagesaveoptions/\#getPageSet) / [ImageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/imagesaveoptions/\#setPageSet-com.aspose.words.PageSet), you can specify a particular set of pages to convert into images.
## Methods

| Method | Description |
| --- | --- |
| [convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convert(InputStream inputStream, OutputStream outputStream, int saveFormat)](#convert-java.io.InputStream-java.io.OutputStream-int) |  |
| [convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions)](#convert-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.SaveOptions) | Converts the given input document into the output document using specified input output file names its load/save options. |
| [convert(String inputFile, String outputFile)](#convert-java.lang.String-java.lang.String) | Converts the given input document into the output document using specified input output file names and its extensions. |
| [convert(String inputFile, String outputFile, SaveOptions saveOptions)](#convert-java.lang.String-java.lang.String-com.aspose.words.SaveOptions) | Converts the given input document into the output document using specified input output file names and save options. |
| [convert(String inputFile, String outputFile, int saveFormat)](#convert-java.lang.String-java.lang.String-int) |  |
| [convertToImages(Document doc, ImageSaveOptions saveOptions)](#convertToImages-com.aspose.words.Document-com.aspose.words.ImageSaveOptions) | Converts the pages of the specified document to images using the specified save options and returns an array of streams containing the images. |
| [convertToImages(Document doc, int saveFormat)](#convertToImages-com.aspose.words.Document-int) |  |
| [convertToImages(InputStream inputStream, ImageSaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions) | Converts the pages of the specified input stream to images using the specified save options and returns an array of streams containing the images. |
| [convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.ImageSaveOptions) | Converts the pages of the specified input stream to images using the provided load and save options, and returns an array of streams containing the images. |
| [convertToImages(InputStream inputStream, int saveFormat)](#convertToImages-java.io.InputStream-int) |  |
| [convertToImages(String inputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-com.aspose.words.ImageSaveOptions) | Converts the pages of the specified input file to images using the specified save options and returns an array of streams containing the images. |
| [convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.ImageSaveOptions) | Converts the pages of the specified input file to image files using the provided load and save options. |
| [convertToImages(String inputFile, int saveFormat)](#convertToImages-java.lang.String-int) |  |
| [convertToImages(String inputFile, String outputFile)](#convertToImages-java.lang.String-java.lang.String) | Converts the pages of the specified input file to image files. |
| [convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions) | Converts the pages of the specified input file to image files using the specified save options. |
| [convertToImages(String inputFile, String outputFile, int saveFormat)](#convertToImages-java.lang.String-java.lang.String-int) |  |
| [create()](#create) | Creates new instance of the converter processor. |
| [create(ConverterContext context)](#create-com.aspose.words.ConverterContext) | Creates new instance of the converter processor. |
| [execute()](#execute) | Execute the processor action. |
| [from(InputStream input)](#from-java.io.InputStream) |  |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Specifies input document for processing. |
| [from(String input)](#from-java.lang.String) |  |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Specifies input document for processing. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) |  |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Specifies output file for the processor. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public static void convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public static void convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convert(InputStream inputStream, OutputStream outputStream, int saveFormat) {#convert-java.io.InputStream-java.io.OutputStream-int}
```
public static void convert(InputStream inputStream, OutputStream outputStream, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |

### convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions) {#convert-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.SaveOptions}
```
public static void convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions)
```


Converts the given input document into the output document using specified input output file names its load/save options.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to convert documents with a single line of code.

```

 String doc = getMyDir() + "Document.docx";

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.pdf");

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveFormat.rtf", SaveFormat.RTF);

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.convert(doc, loadOptions, getArtifactsDir() + "LowCode.Convert.LoadOptions.docx", saveOptions);

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveOptions.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | java.lang.String | The input file name. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | The input document load options. |
| outputFile | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The save options. |

### convert(String inputFile, String outputFile) {#convert-java.lang.String-java.lang.String}
```
public static void convert(String inputFile, String outputFile)
```


Converts the given input document into the output document using specified input output file names and its extensions.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to convert documents with a single line of code.

```

 String doc = getMyDir() + "Document.docx";

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.pdf");

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveFormat.rtf", SaveFormat.RTF);

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.convert(doc, loadOptions, getArtifactsDir() + "LowCode.Convert.LoadOptions.docx", saveOptions);

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveOptions.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | java.lang.String | The input file name. |
| outputFile | java.lang.String | The output file name. |

### convert(String inputFile, String outputFile, SaveOptions saveOptions) {#convert-java.lang.String-java.lang.String-com.aspose.words.SaveOptions}
```
public static void convert(String inputFile, String outputFile, SaveOptions saveOptions)
```


Converts the given input document into the output document using specified input output file names and save options.

 **Remarks:** 

If the output format is an image (BMP, EMF, EPS, GIF, JPEG, PNG, or WebP), each page of the output will be saved as a separate file. The specified output file name will be used to generate file names for each part following the rule: outputFile\_partIndex.extension.

If the output format is TIFF, the output will be saved as a single multi-frame TIFF file.

 **Examples:** 

Shows how to convert documents with a single line of code.

```

 String doc = getMyDir() + "Document.docx";

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.pdf");

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveFormat.rtf", SaveFormat.RTF);

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.convert(doc, loadOptions, getArtifactsDir() + "LowCode.Convert.LoadOptions.docx", saveOptions);

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveOptions.docx", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | java.lang.String | The input file name. |
| outputFile | java.lang.String | The output file name. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | The save options. |

### convert(String inputFile, String outputFile, int saveFormat) {#convert-java.lang.String-java.lang.String-int}
```
public static void convert(String inputFile, String outputFile, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| outputFile | java.lang.String |  |
| saveFormat | int |  |

### convertToImages(Document doc, ImageSaveOptions saveOptions) {#convertToImages-com.aspose.words.Document-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(Document doc, ImageSaveOptions saveOptions)
```


Converts the pages of the specified document to images using the specified save options and returns an array of streams containing the images.

 **Examples:** 

Shows how to convert document to images stream.

```

 String doc = getMyDir() + "Big document.docx";

 OutputStream[] streams = Converter.convertToImages(doc, SaveFormat.PNG);

 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 streams = Converter.convertToImages(doc, imageSaveOptions);

 streams = Converter.convertToImages(new Document(doc), SaveFormat.PNG);

 streams = Converter.convertToImages(new Document(doc), imageSaveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | The input document. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Image save options. |

**Returns:**
java.io.OutputStream[] - Returns array of image streams. The streams should be disposed by the end user.
### convertToImages(Document doc, int saveFormat) {#convertToImages-com.aspose.words.Document-int}
```
public static OutputStream[] convertToImages(Document doc, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(InputStream inputStream, ImageSaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(InputStream inputStream, ImageSaveOptions saveOptions)
```


Converts the pages of the specified input stream to images using the specified save options and returns an array of streams containing the images.

 **Examples:** 

Shows how to convert document to images from stream.

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx")) {
     OutputStream[] streams = Converter.convertToImages(streamIn, SaveFormat.JPEG);

     ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
     imageSaveOptions.setPageSet(new PageSet(1));
     streams = Converter.convertToImages(streamIn, imageSaveOptions);

     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(false);
     }
     Converter.convertToImages(streamIn, loadOptions, imageSaveOptions);
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Image save options. |

**Returns:**
java.io.OutputStream[] - Returns array of image streams. The streams should be disposed by the end user.
### convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions)
```


Converts the pages of the specified input stream to images using the provided load and save options, and returns an array of streams containing the images.

 **Examples:** 

Shows how to convert document to images from stream.

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx")) {
     OutputStream[] streams = Converter.convertToImages(streamIn, SaveFormat.JPEG);

     ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
     imageSaveOptions.setPageSet(new PageSet(1));
     streams = Converter.convertToImages(streamIn, imageSaveOptions);

     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(false);
     }
     Converter.convertToImages(streamIn, loadOptions, imageSaveOptions);
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input stream. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | The input document load options. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Image save options. |

**Returns:**
java.io.OutputStream[] - Returns array of image streams. The streams should be disposed by the end user.
### convertToImages(InputStream inputStream, int saveFormat) {#convertToImages-java.io.InputStream-int}
```
public static OutputStream[] convertToImages(InputStream inputStream, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(String inputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(String inputFile, ImageSaveOptions saveOptions)
```


Converts the pages of the specified input file to images using the specified save options and returns an array of streams containing the images.

 **Examples:** 

Shows how to convert document to images stream.

```

 String doc = getMyDir() + "Big document.docx";

 OutputStream[] streams = Converter.convertToImages(doc, SaveFormat.PNG);

 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 streams = Converter.convertToImages(doc, imageSaveOptions);

 streams = Converter.convertToImages(new Document(doc), SaveFormat.PNG);

 streams = Converter.convertToImages(new Document(doc), imageSaveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Image save options. |

**Returns:**
java.io.OutputStream[] - Returns array of image streams. The streams should be disposed by the end user.
### convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static void convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions)
```


Converts the pages of the specified input file to image files using the provided load and save options.

 **Examples:** 

Shows how to convert document to images.

```

 String doc = getMyDir() + "Big document.docx";

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.1.png");

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.2.jpeg", SaveFormat.JPEG);

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(false);
 }
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 Converter.convertToImages(doc, loadOptions, getArtifactsDir() + "LowCode.ConvertToImages.3.png", imageSaveOptions);

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.4.png", imageSaveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | java.lang.String | The input file name. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | The input document load options. |
| outputFile | java.lang.String | The output file name used to generate file name for page images using rule "outputFile\_pageIndex.extension" |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Image save options. |

### convertToImages(String inputFile, int saveFormat) {#convertToImages-java.lang.String-int}
```
public static OutputStream[] convertToImages(String inputFile, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(String inputFile, String outputFile) {#convertToImages-java.lang.String-java.lang.String}
```
public static void convertToImages(String inputFile, String outputFile)
```


Converts the pages of the specified input file to image files.

 **Examples:** 

Shows how to convert document to images.

```

 String doc = getMyDir() + "Big document.docx";

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.1.png");

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.2.jpeg", SaveFormat.JPEG);

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(false);
 }
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 Converter.convertToImages(doc, loadOptions, getArtifactsDir() + "LowCode.ConvertToImages.3.png", imageSaveOptions);

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.4.png", imageSaveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | java.lang.String | The input file name. |
| outputFile | java.lang.String | The output file name used to generate file name for page images using rule "outputFile\_pageIndex.extension" |

### convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static void convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions)
```


Converts the pages of the specified input file to image files using the specified save options.

 **Examples:** 

Shows how to convert document to images.

```

 String doc = getMyDir() + "Big document.docx";

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.1.png");

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.2.jpeg", SaveFormat.JPEG);

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(false);
 }
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 Converter.convertToImages(doc, loadOptions, getArtifactsDir() + "LowCode.ConvertToImages.3.png", imageSaveOptions);

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.4.png", imageSaveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | java.lang.String | The input file name. |
| outputFile | java.lang.String | The output file name used to generate file name for page images using rule "outputFile\_pageIndex.extension" |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Image save options. |

### convertToImages(String inputFile, String outputFile, int saveFormat) {#convertToImages-java.lang.String-java.lang.String-int}
```
public static void convertToImages(String inputFile, String outputFile, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| outputFile | java.lang.String |  |
| saveFormat | int |  |

### create() {#create}
```
public static Converter create()
```


Creates new instance of the converter processor.

**Returns:**
[Converter](../../com.aspose.words/converter/)
### create(ConverterContext context) {#create-com.aspose.words.ConverterContext}
```
public static Converter create(ConverterContext context)
```


Creates new instance of the converter processor.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| context | [ConverterContext](../../com.aspose.words/convertercontext/) |  |

**Returns:**
[Converter](../../com.aspose.words/converter/)
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
