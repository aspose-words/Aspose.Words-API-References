---
title: "PageExtractOptions"
linktitle: "PageExtractOptions"
second_title: "Aspose.Words Java için"
description: "Java'da belge sayfası çıkarma seçeneklerini belirtmeye olanak tanır."
type: docs
weight: 512
url: /tr/java/com.aspose.words/pageextractoptions/
---

**Inheritance:**
java.lang.Object
```
public class PageExtractOptions
```

Belge sayfası çıkarma için seçenekleri belirtmeye olanak tanır.

 **Examples:** 

İlk sayfa numaralandırmasını nasıl sıfırlayacağınızı ve NUMPAGE alanını nasıl kaydedeceğinizi gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [PageExtractOptions()](#PageExtractOptions) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getUnlinkPagesNumberFields()](#getUnlinkPagesNumberFields) | Sonuç belgesindeki NUMPAGES alanlarının gerçek sonuç değerleriyle değiştirilip değiştirilmeyeceğini belirtir. |
| [getUpdatePageStartingNumber()](#getUpdatePageStartingNumber) | Sonuç belgesindeki başlangıç sayfa numarasının güncellenip güncellenmeyeceğini belirtir. |
| [setUnlinkPagesNumberFields(boolean value)](#setUnlinkPagesNumberFields-boolean) | Sonuç belgesindeki NUMPAGES alanlarının gerçek sonuç değerleriyle değiştirilip değiştirilmeyeceğini belirtir. |
| [setUpdatePageStartingNumber(boolean value)](#setUpdatePageStartingNumber-boolean) | Sonuç belgesindeki başlangıç sayfa numarasının güncellenip güncellenmeyeceğini belirtir. |
### PageExtractOptions() {#PageExtractOptions}
```
public PageExtractOptions()
```


Bu sınıfın yeni bir örneğini başlatır.

### getUnlinkPagesNumberFields() {#getUnlinkPagesNumberFields}
```
public boolean getUnlinkPagesNumberFields()
```


Sonuç belgesindeki NUMPAGES alanlarının gerçek sonuç değerleriyle değiştirilip değiştirilmeyeceğini belirtir. Varsayılan değer true'dir.

 **Examples:** 

İlk sayfa numaralandırmasını nasıl sıfırlayacağınızı ve NUMPAGE alanını nasıl kaydedeceğinizi gösterir.

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
boolean - İlgili  boolean  değeri.
### getUpdatePageStartingNumber() {#getUpdatePageStartingNumber}
```
public boolean getUpdatePageStartingNumber()
```


Sonuç belgesindeki başlangıç sayfa numarasının güncellenip güncellenmeyeceğini belirtir. Varsayılan değer true'dir.

 **Examples:** 

İlk sayfa numaralandırmasını nasıl sıfırlayacağınızı ve NUMPAGE alanını nasıl kaydedeceğinizi gösterir.

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
boolean - İlgili  boolean  değeri.
### setUnlinkPagesNumberFields(boolean value) {#setUnlinkPagesNumberFields-boolean}
```
public void setUnlinkPagesNumberFields(boolean value)
```


Sonuç belgesindeki NUMPAGES alanlarının gerçek sonuç değerleriyle değiştirilip değiştirilmeyeceğini belirtir. Varsayılan değer true'dir.

 **Examples:** 

İlk sayfa numaralandırmasını nasıl sıfırlayacağınızı ve NUMPAGE alanını nasıl kaydedeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setUpdatePageStartingNumber(boolean value) {#setUpdatePageStartingNumber-boolean}
```
public void setUpdatePageStartingNumber(boolean value)
```


Sonuç belgesindeki başlangıç sayfa numarasının güncellenip güncellenmeyeceğini belirtir. Varsayılan değer true'dir.

 **Examples:** 

İlk sayfa numaralandırmasını nasıl sıfırlayacağınızı ve NUMPAGE alanını nasıl kaydedeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

