---
title: Splitter
linktitle: Splitter
second_title: Aspose.Words for Java
description: Provides methods intended to split the documents into parts using different criteria in Java.
type: docs
weight: 605
url: /java/com.aspose.words/splitter/
---

**Inheritance:**
java.lang.Object
```
public class Splitter
```

Provides methods intended to split the documents into parts using different criteria.
## Methods

| Method | Description |
| --- | --- |
| [extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount)](#extractPages-java.io.InputStream-java.io.OutputStream-int-int-int) |  |
| [extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-int-int) | Extracts a specified range of pages from a document file and saves the extracted pages to a new file. |
| [extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount)](#extractPages-java.lang.String-java.lang.String-int-int-int) |  |
| [removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat)](#removeBlankPages-java.io.InputStream-java.io.OutputStream-int) |  |
| [removeBlankPages(String inputFileName, String outputFileName)](#removeBlankPages-java.lang.String-java.lang.String) | Removes empty pages from the document and saves the output. |
| [removeBlankPages(String inputFileName, String outputFileName, int saveFormat)](#removeBlankPages-java.lang.String-java.lang.String-int) |  |
| [split(InputStream inputStream, int saveFormat, SplitOptions options)](#split-java.io.InputStream-int-com.aspose.words.SplitOptions) |  |
| [split(String inputFileName, String outputFileName, SplitOptions options)](#split-java.lang.String-java.lang.String-com.aspose.words.SplitOptions) | Splits a document into multiple parts based on the specified split options and saves the resulting parts to files. |
| [split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options)](#split-java.lang.String-java.lang.String-int-com.aspose.words.SplitOptions) |  |
### extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount) {#extractPages-java.io.InputStream-java.io.OutputStream-int-int-int}
```
public static void extractPages(InputStream inputStream, OutputStream outputStream, int saveFormat, int startPageIndex, int pageCount)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| startPageIndex | int |  |
| pageCount | int |  |

### extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, int startPageIndex, int pageCount)
```


Extracts a specified range of pages from a document file and saves the extracted pages to a new file. The output file format is determined by the extension of the output file name.

 **Examples:** 

Shows how to extract pages from the document.

```

 // There is a several ways to extract pages from the document:
 String doc = getMyDir() + "Big document.docx";

 Splitter.extractPages(doc, getArtifactsDir() + "LowCode.ExtractPages.1.docx", 0, 2);
 Splitter.extractPages(doc, getArtifactsDir() + "LowCode.ExtractPages.2.docx", SaveFormat.DOCX, 0, 2);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |
| startPageIndex | int | The zero-based index of the first page to extract. |
| pageCount | int | Number of pages to be extracted. |

### extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount) {#extractPages-java.lang.String-java.lang.String-int-int-int}
```
public static void extractPages(String inputFileName, String outputFileName, int saveFormat, int startPageIndex, int pageCount)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| startPageIndex | int |  |
| pageCount | int |  |

### removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat) {#removeBlankPages-java.io.InputStream-java.io.OutputStream-int}
```
public static ArrayList removeBlankPages(InputStream inputStream, OutputStream outputStream, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
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


Removes empty pages from the document and saves the output. Returns a list of page numbers that were removed.

 **Examples:** 

Shows how to remove empty pages from the document.

```

 // There is a several ways to remove empty pages from the document:
 String doc = getMyDir() + "Blank pages.docx";

 Splitter.removeBlankPages(doc, getArtifactsDir() + "LowCode.RemoveBlankPages.1.docx");
 Splitter.removeBlankPages(doc, getArtifactsDir() + "LowCode.RemoveBlankPages.2.docx", SaveFormat.DOCX);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name. |

**Returns:**
java.util.ArrayList - List of page numbers has been considered as blank and removed.
### removeBlankPages(String inputFileName, String outputFileName, int saveFormat) {#removeBlankPages-java.lang.String-java.lang.String-int}
```
public static ArrayList removeBlankPages(String inputFileName, String outputFileName, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
java.util.ArrayList
### split(InputStream inputStream, int saveFormat, SplitOptions options) {#split-java.io.InputStream-int-com.aspose.words.SplitOptions}
```
public static InputStream[] split(InputStream inputStream, int saveFormat, SplitOptions options)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveFormat | int |  |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) |  |

**Returns:**
java.io.InputStream[]
### split(String inputFileName, String outputFileName, SplitOptions options) {#split-java.lang.String-java.lang.String-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, SplitOptions options)
```


Splits a document into multiple parts based on the specified split options and saves the resulting parts to files. The output file format is determined by the extension of the output file name.

 **Examples:** 

Shows how to split document by pages.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | The input file name. |
| outputFileName | java.lang.String | The output file name used to generate file name for document parts using rule "outputFile\_partIndex.extension" |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) | Document split options. |

### split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options) {#split-java.lang.String-java.lang.String-int-com.aspose.words.SplitOptions}
```
public static void split(String inputFileName, String outputFileName, int saveFormat, SplitOptions options)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| options | [SplitOptions](../../com.aspose.words/splitoptions/) |  |

