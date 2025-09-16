---
title: PageExtractOptions
linktitle: PageExtractOptions
second_title: Aspose.Words for Java
description: Allows to specify options for document page extracting in Java.
type: docs
weight: 510
url: /java/com.aspose.words/pageextractoptions/
---

**Inheritance:**
java.lang.Object
```
public class PageExtractOptions
```

Allows to specify options for document page extracting.

 **Examples:** 

Show how to reset the initial page numbering and save the NUMPAGE field.

```

 Document doc = new Document(getMyDir() + "Page fields.docx");

 // Default behavior:
 // The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
 // The start page will be set to 2 and the field indicating the number of pages will be removed
 // and replaced with a constant value equal to the number of pages.
 Document extractedDoc1 = doc.extractPages(1, 1);
 extractedDoc1.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Default.docx");

 // Altered behavior:
 // The extracted page numbering is reset and a new one begins,
 // as if we had copied the contents of the second page and pasted it into a new document.
 // The start page will be set to 1 and the field indicating the number of pages will be left unchanged
 // and will show the current number of pages.
 PageExtractOptions extractOptions = new PageExtractOptions();
 extractOptions.setUpdatePageStartingNumber(false);
 extractOptions.setUnlinkPagesNumberFields(false);
 Document extractedDoc2 = doc.extractPages(1, 1, extractOptions);
 extractedDoc2.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Options.docx");
 
```
## Constructors

| Constructor | Description |
| --- | --- |
| [PageExtractOptions()](#PageExtractOptions) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getUnlinkPagesNumberFields()](#getUnlinkPagesNumberFields) | Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values. |
| [getUpdatePageStartingNumber()](#getUpdatePageStartingNumber) | Specifies whether the start page number in the resulting document shall be updated. |
| [setUnlinkPagesNumberFields(boolean value)](#setUnlinkPagesNumberFields-boolean) | Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values. |
| [setUpdatePageStartingNumber(boolean value)](#setUpdatePageStartingNumber-boolean) | Specifies whether the start page number in the resulting document shall be updated. |
### PageExtractOptions() {#PageExtractOptions}
```
public PageExtractOptions()
```


Initializes a new instance of this class.

### getUnlinkPagesNumberFields() {#getUnlinkPagesNumberFields}
```
public boolean getUnlinkPagesNumberFields()
```


Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values. Default value is  true .

 **Examples:** 

Show how to reset the initial page numbering and save the NUMPAGE field.

```

 Document doc = new Document(getMyDir() + "Page fields.docx");

 // Default behavior:
 // The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
 // The start page will be set to 2 and the field indicating the number of pages will be removed
 // and replaced with a constant value equal to the number of pages.
 Document extractedDoc1 = doc.extractPages(1, 1);
 extractedDoc1.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Default.docx");

 // Altered behavior:
 // The extracted page numbering is reset and a new one begins,
 // as if we had copied the contents of the second page and pasted it into a new document.
 // The start page will be set to 1 and the field indicating the number of pages will be left unchanged
 // and will show the current number of pages.
 PageExtractOptions extractOptions = new PageExtractOptions();
 extractOptions.setUpdatePageStartingNumber(false);
 extractOptions.setUnlinkPagesNumberFields(false);
 Document extractedDoc2 = doc.extractPages(1, 1, extractOptions);
 extractedDoc2.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Options.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getUpdatePageStartingNumber() {#getUpdatePageStartingNumber}
```
public boolean getUpdatePageStartingNumber()
```


Specifies whether the start page number in the resulting document shall be updated. Default value is  true .

 **Examples:** 

Show how to reset the initial page numbering and save the NUMPAGE field.

```

 Document doc = new Document(getMyDir() + "Page fields.docx");

 // Default behavior:
 // The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
 // The start page will be set to 2 and the field indicating the number of pages will be removed
 // and replaced with a constant value equal to the number of pages.
 Document extractedDoc1 = doc.extractPages(1, 1);
 extractedDoc1.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Default.docx");

 // Altered behavior:
 // The extracted page numbering is reset and a new one begins,
 // as if we had copied the contents of the second page and pasted it into a new document.
 // The start page will be set to 1 and the field indicating the number of pages will be left unchanged
 // and will show the current number of pages.
 PageExtractOptions extractOptions = new PageExtractOptions();
 extractOptions.setUpdatePageStartingNumber(false);
 extractOptions.setUnlinkPagesNumberFields(false);
 Document extractedDoc2 = doc.extractPages(1, 1, extractOptions);
 extractedDoc2.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Options.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### setUnlinkPagesNumberFields(boolean value) {#setUnlinkPagesNumberFields-boolean}
```
public void setUnlinkPagesNumberFields(boolean value)
```


Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values. Default value is  true .

 **Examples:** 

Show how to reset the initial page numbering and save the NUMPAGE field.

```

 Document doc = new Document(getMyDir() + "Page fields.docx");

 // Default behavior:
 // The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
 // The start page will be set to 2 and the field indicating the number of pages will be removed
 // and replaced with a constant value equal to the number of pages.
 Document extractedDoc1 = doc.extractPages(1, 1);
 extractedDoc1.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Default.docx");

 // Altered behavior:
 // The extracted page numbering is reset and a new one begins,
 // as if we had copied the contents of the second page and pasted it into a new document.
 // The start page will be set to 1 and the field indicating the number of pages will be left unchanged
 // and will show the current number of pages.
 PageExtractOptions extractOptions = new PageExtractOptions();
 extractOptions.setUpdatePageStartingNumber(false);
 extractOptions.setUnlinkPagesNumberFields(false);
 Document extractedDoc2 = doc.extractPages(1, 1, extractOptions);
 extractedDoc2.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Options.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setUpdatePageStartingNumber(boolean value) {#setUpdatePageStartingNumber-boolean}
```
public void setUpdatePageStartingNumber(boolean value)
```


Specifies whether the start page number in the resulting document shall be updated. Default value is  true .

 **Examples:** 

Show how to reset the initial page numbering and save the NUMPAGE field.

```

 Document doc = new Document(getMyDir() + "Page fields.docx");

 // Default behavior:
 // The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
 // The start page will be set to 2 and the field indicating the number of pages will be removed
 // and replaced with a constant value equal to the number of pages.
 Document extractedDoc1 = doc.extractPages(1, 1);
 extractedDoc1.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Default.docx");

 // Altered behavior:
 // The extracted page numbering is reset and a new one begins,
 // as if we had copied the contents of the second page and pasted it into a new document.
 // The start page will be set to 1 and the field indicating the number of pages will be left unchanged
 // and will show the current number of pages.
 PageExtractOptions extractOptions = new PageExtractOptions();
 extractOptions.setUpdatePageStartingNumber(false);
 extractOptions.setUnlinkPagesNumberFields(false);
 Document extractedDoc2 = doc.extractPages(1, 1, extractOptions);
 extractedDoc2.save(getArtifactsDir() + "Document.ExtractPagesWithOptions.Options.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

