---
title: ComparerContext
linktitle: ComparerContext
second_title: Aspose.Words for Java
description: Document comparer context in Java.
type: docs
weight: 115
url: /java/com.aspose.words/comparercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ComparerContext extends ProcessorContext
```

Document comparer context

 **Examples:** 

Shows how to simple compare documents using context.

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

Shows how to compare documents from the stream using context.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [ComparerContext()](#ComparerContext) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getAcceptRevisions()](#getAcceptRevisions) | Indicates whether to accept revisions in the documents before comparing them. |
| [getAuthor()](#getAuthor) | The author to be assigned to revisions created during document comparison. |
| [getCompareOptions()](#getCompareOptions) | Options used upon comparing documents. |
| [getDateTime()](#getDateTime) | The date and time assigned to revisions created during document comparison. |
| [getFontSettings()](#getFontSettings) | Font settings used by the processor. |
| [getLayoutOptions()](#getLayoutOptions) | Document layout options used by the processor. |
| [getWarningCallback()](#getWarningCallback) | Warning callback used by the processor. |
| [setAcceptRevisions(boolean value)](#setAcceptRevisions-boolean) | Indicates whether to accept revisions in the documents before comparing them. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | The author to be assigned to revisions created during document comparison. |
| [setDateTime(Date value)](#setDateTime-java.util.Date) | The date and time assigned to revisions created during document comparison. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Font settings used by the processor. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Warning callback used by the processor. |
### ComparerContext() {#ComparerContext}
```
public ComparerContext()
```


Initializes a new instance of this class.

### getAcceptRevisions() {#getAcceptRevisions}
```
public boolean getAcceptRevisions()
```


Indicates whether to accept revisions in the documents before comparing them. If the compared documents contain revisions and this flag is set to false, the processor will reject revisions. Default is  true .

**Returns:**
boolean - The corresponding  boolean  value.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


The author to be assigned to revisions created during document comparison.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getCompareOptions() {#getCompareOptions}
```
public CompareOptions getCompareOptions()
```


Options used upon comparing documents.

 **Examples:** 

Shows how to simple compare documents using context.

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

Shows how to compare documents from the stream using context.

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

**Returns:**
[CompareOptions](../../com.aspose.words/compareoptions/) - The corresponding [CompareOptions](../../com.aspose.words/compareoptions/) value.
### getDateTime() {#getDateTime}
```
public Date getDateTime()
```


The date and time assigned to revisions created during document comparison.

**Returns:**
java.util.Date - The corresponding java.util.Date value.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Font settings used by the processor.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Document layout options used by the processor.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Warning callback used by the processor.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setAcceptRevisions(boolean value) {#setAcceptRevisions-boolean}
```
public void setAcceptRevisions(boolean value)
```


Indicates whether to accept revisions in the documents before comparing them. If the compared documents contain revisions and this flag is set to false, the processor will reject revisions. Default is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


The author to be assigned to revisions created during document comparison.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setDateTime(Date value) {#setDateTime-java.util.Date}
```
public void setDateTime(Date value)
```


The date and time assigned to revisions created during document comparison.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date | The corresponding java.util.Date value. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Font settings used by the processor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Warning callback used by the processor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value. |

