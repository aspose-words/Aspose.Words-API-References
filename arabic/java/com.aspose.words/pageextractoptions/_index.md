---
title: "PageExtractOptions"
linktitle: "PageExtractOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد خيارات استخراج صفحات المستند في Java."
type: docs
weight: 512
url: /ar/java/com.aspose.words/pageextractoptions/
---

**Inheritance:**
java.lang.Object
```
public class PageExtractOptions
```

يسمح بتحديد خيارات استخراج صفحات المستند.

 **Examples:** 

يظهر كيفية إعادة تعيين ترقيم الصفحات الأولي وحفظ الحقل NUMPAGE.

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [PageExtractOptions()](#PageExtractOptions) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getUnlinkPagesNumberFields()](#getUnlinkPagesNumberFields) | يحدد ما إذا كانت حقول NUMPAGES في المستند الناتج سيتم استبدالها بالقيم الفعلية الناتجة. |
| [getUpdatePageStartingNumber()](#getUpdatePageStartingNumber) | يحدد ما إذا كان رقم الصفحة البداية في المستند الناتج يجب تحديثه. |
| [setUnlinkPagesNumberFields(boolean value)](#setUnlinkPagesNumberFields-boolean) | يحدد ما إذا كانت حقول NUMPAGES في المستند الناتج سيتم استبدالها بالقيم الفعلية الناتجة. |
| [setUpdatePageStartingNumber(boolean value)](#setUpdatePageStartingNumber-boolean) | يحدد ما إذا كان رقم الصفحة البداية في المستند الناتج يجب تحديثه. |
### PageExtractOptions() {#PageExtractOptions}
```
public PageExtractOptions()
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

### getUnlinkPagesNumberFields() {#getUnlinkPagesNumberFields}
```
public boolean getUnlinkPagesNumberFields()
```


يحدد ما إذا كانت حقول NUMPAGES في المستند الناتج سيتم استبدالها بالقيم الفعلية الناتجة. القيمة الافتراضية هي  true .

 **Examples:** 

يظهر كيفية إعادة تعيين ترقيم الصفحات الأولي وحفظ الحقل NUMPAGE.

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
boolean - القيمة المنطقية المقابلة.
### getUpdatePageStartingNumber() {#getUpdatePageStartingNumber}
```
public boolean getUpdatePageStartingNumber()
```


يحدد ما إذا كان رقم الصفحة البداية في المستند الناتج يجب تحديثه. القيمة الافتراضية هي  true .

 **Examples:** 

يظهر كيفية إعادة تعيين ترقيم الصفحات الأولي وحفظ الحقل NUMPAGE.

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
boolean - القيمة المنطقية المقابلة.
### setUnlinkPagesNumberFields(boolean value) {#setUnlinkPagesNumberFields-boolean}
```
public void setUnlinkPagesNumberFields(boolean value)
```


يحدد ما إذا كانت حقول NUMPAGES في المستند الناتج سيتم استبدالها بالقيم الفعلية الناتجة. القيمة الافتراضية هي  true .

 **Examples:** 

يظهر كيفية إعادة تعيين ترقيم الصفحات الأولي وحفظ الحقل NUMPAGE.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setUpdatePageStartingNumber(boolean value) {#setUpdatePageStartingNumber-boolean}
```
public void setUpdatePageStartingNumber(boolean value)
```


يحدد ما إذا كان رقم الصفحة البداية في المستند الناتج يجب تحديثه. القيمة الافتراضية هي  true .

 **Examples:** 

يظهر كيفية إعادة تعيين ترقيم الصفحات الأولي وحفظ الحقل NUMPAGE.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

