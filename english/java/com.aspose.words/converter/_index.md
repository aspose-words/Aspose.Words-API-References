---
title: Converter
linktitle: Converter
second_title: Aspose.Words for Java
description: Represents a group of methods intended to convert a variety of different types of documents using a single line of code in Java.
type: docs
weight: 122
url: /java/com.aspose.words/converter/
---

**Inheritance:**
java.lang.Object
```
public class Converter
```

Represents a group of methods intended to convert a variety of different types of documents using a single line of code.

 **Remarks:** 

The specified input and output files or streams, along with the desired save format, are used to convert the given input document of the one format into the output document of the other specified format.

The convert functionality supports over 35+ different file formats.

The [convertToImages(java.lang.String, java.lang.String)](../../com.aspose.words/converter/\#convertToImages-java.lang.String--java.lang.String) group of methods are designed to transform documents into images, with each page being converted into a separate image file. These methods also convert PDF documents directly to fixed-page formats without loading them into the document model (using our pdf2word plugin), which enhances both performance and accuracy.

With [ImageSaveOptions.getPageSet()](../../com.aspose.words/imagesaveoptions/\#getPageSet) / [ImageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/imagesaveoptions/\#setPageSet-com.aspose.words.PageSet), you can specify a particular set of pages to convert into images.
## Methods

| Method | Description |
| --- | --- |
| [convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convert(InputStream inputStream, OutputStream outputStream, int saveFormat)](#convert-java.io.InputStream-java.io.OutputStream-int) |  |
| [convert(String inputFile, String outputFile)](#convert-java.lang.String-java.lang.String) | Converts the given input document into the output document using specified input output file names and its extensions. |
| [convert(String inputFile, String outputFile, SaveOptions saveOptions)](#convert-java.lang.String-java.lang.String-com.aspose.words.SaveOptions) | Converts the given input document into the output document using specified input output file names and save options. |
| [convert(String inputFile, String outputFile, int saveFormat)](#convert-java.lang.String-java.lang.String-int) |  |
| [convertToImages(Document doc, ImageSaveOptions saveOptions)](#convertToImages-com.aspose.words.Document-com.aspose.words.ImageSaveOptions) | Converts the document pages to images. |
| [convertToImages(Document doc, int saveFormat)](#convertToImages-com.aspose.words.Document-int) |  |
| [convertToImages(InputStream inputStream, ImageSaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions) | Converts the input stream pages to images. |
| [convertToImages(InputStream inputStream, int saveFormat)](#convertToImages-java.io.InputStream-int) |  |
| [convertToImages(String inputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-com.aspose.words.ImageSaveOptions) | Converts the input file pages to images. |
| [convertToImages(String inputFile, int saveFormat)](#convertToImages-java.lang.String-int) |  |
| [convertToImages(String inputFile, String outputFile)](#convertToImages-java.lang.String-java.lang.String) | Converts the input file pages to images. |
| [convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions) | Converts the input file pages to images. |
| [convertToImages(String inputFile, String outputFile, int saveFormat)](#convertToImages-java.lang.String-java.lang.String-int) |  |
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

### convert(String inputFile, String outputFile) {#convert-java.lang.String-java.lang.String}
```
public static void convert(String inputFile, String outputFile)
```


Converts the given input document into the output document using specified input output file names and its extensions.

 **Examples:** 

Shows how to convert documents with a single line of code.

```

 Converter.convert(getMyDir() + "Document.docx", getArtifactsDir() + "LowCode.Convert.pdf");

 Converter.convert(getMyDir() + "Document.docx", getArtifactsDir() + "LowCode.Convert.rtf", SaveFormat.RTF);

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setPassword("Aspose.Words"); }
 Converter.convert(getMyDir() + "Document.doc", getArtifactsDir() + "LowCode.Convert.docx", saveOptions);
 
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

 **Examples:** 

Shows how to convert documents with a single line of code.

```

 Converter.convert(getMyDir() + "Document.docx", getArtifactsDir() + "LowCode.Convert.pdf");

 Converter.convert(getMyDir() + "Document.docx", getArtifactsDir() + "LowCode.Convert.rtf", SaveFormat.RTF);

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setPassword("Aspose.Words"); }
 Converter.convert(getMyDir() + "Document.doc", getArtifactsDir() + "LowCode.Convert.docx", saveOptions);
 
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
public static InputStream[] convertToImages(Document doc, ImageSaveOptions saveOptions)
```


Converts the document pages to images.

 **Examples:** 

Shows how to convert document to images stream.

```

 Stream[] streams = Converter.convertToImages(getMyDir() + "Big document.docx", SaveFormat.PNG);

 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 streams = Converter.convertToImages(getMyDir() + "Big document.docx", imageSaveOptions);

 streams = Converter.convertToImages(new Document(getMyDir() + "Big document.docx"), SaveFormat.PNG);

 streams = Converter.convertToImages(new Document(getMyDir() + "Big document.docx"), imageSaveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | The input document. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Image save options. |

**Returns:**
java.io.InputStream[] - Returns array of image streams. The streams should be disposed by the enduser.
### convertToImages(Document doc, int saveFormat) {#convertToImages-com.aspose.words.Document-int}
```
public static InputStream[] convertToImages(Document doc, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| saveFormat | int |  |

**Returns:**
java.io.InputStream[]
### convertToImages(InputStream inputStream, ImageSaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions}
```
public static InputStream[] convertToImages(InputStream inputStream, ImageSaveOptions saveOptions)
```


Converts the input stream pages to images.

 **Examples:** 

Shows how to convert document to images from stream.

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx"))
 {
     Stream[] streams = Converter.convertToImages(streamIn, SaveFormat.JPEG);

     ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
     imageSaveOptions.setPageSet(new PageSet(1));
     streams = Converter.convertToImages(streamIn, imageSaveOptions);
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | The input stream. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Image save options. |

**Returns:**
java.io.InputStream[] - Returns array of image streams. The streams should be disposed by the enduser.
### convertToImages(InputStream inputStream, int saveFormat) {#convertToImages-java.io.InputStream-int}
```
public static InputStream[] convertToImages(InputStream inputStream, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveFormat | int |  |

**Returns:**
java.io.InputStream[]
### convertToImages(String inputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static InputStream[] convertToImages(String inputFile, ImageSaveOptions saveOptions)
```


Converts the input file pages to images.

 **Examples:** 

Shows how to convert document to images stream.

```

 Stream[] streams = Converter.convertToImages(getMyDir() + "Big document.docx", SaveFormat.PNG);

 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 streams = Converter.convertToImages(getMyDir() + "Big document.docx", imageSaveOptions);

 streams = Converter.convertToImages(new Document(getMyDir() + "Big document.docx"), SaveFormat.PNG);

 streams = Converter.convertToImages(new Document(getMyDir() + "Big document.docx"), imageSaveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | java.lang.String | The input file name. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Image save options. |

**Returns:**
java.io.InputStream[] - Returns array of image streams. The streams should be disposed by the enduser.
### convertToImages(String inputFile, int saveFormat) {#convertToImages-java.lang.String-int}
```
public static InputStream[] convertToImages(String inputFile, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
java.io.InputStream[]
### convertToImages(String inputFile, String outputFile) {#convertToImages-java.lang.String-java.lang.String}
```
public static void convertToImages(String inputFile, String outputFile)
```


Converts the input file pages to images.

 **Examples:** 

Shows how to convert document to images.

```

 Converter.convertToImages(getMyDir() + "Big document.docx", getArtifactsDir() + "LowCode.ConvertToImages.png");

 Converter.convertToImages(getMyDir() + "Big document.docx", getArtifactsDir() + "LowCode.ConvertToImages.jpeg", SaveFormat.JPEG);

 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 Converter.convertToImages(getMyDir() + "Big document.docx", getArtifactsDir() + "LowCode.ConvertToImages.png", imageSaveOptions);
 
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


Converts the input file pages to images.

 **Examples:** 

Shows how to convert document to images.

```

 Converter.convertToImages(getMyDir() + "Big document.docx", getArtifactsDir() + "LowCode.ConvertToImages.png");

 Converter.convertToImages(getMyDir() + "Big document.docx", getArtifactsDir() + "LowCode.ConvertToImages.jpeg", SaveFormat.JPEG);

 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 Converter.convertToImages(getMyDir() + "Big document.docx", getArtifactsDir() + "LowCode.ConvertToImages.png", imageSaveOptions);
 
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

