---
title: "PageExtractOptions"
linktitle: "PageExtractOptions"
second_title: "Aspose.Words for Java"
description: "允许在 Java 中指定文档页面提取的选项。"
type: docs
weight: 512
url: /zh/java/com.aspose.words/pageextractoptions/
---

**Inheritance:**
java.lang.Object
```
public class PageExtractOptions
```

允许指定文档页面提取的选项。

 **Examples:** 

展示如何重置初始页码并保存 NUMPAGE 字段。

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
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [PageExtractOptions()](#PageExtractOptions) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [getUnlinkPagesNumberFields()](#getUnlinkPagesNumberFields) | 指定是否在生成的文档中将 NUMPAGES 字段替换为其实际的结果值。 |
| [getUpdatePageStartingNumber()](#getUpdatePageStartingNumber) | 指定是否在生成的文档中更新起始页码。 |
| [setUnlinkPagesNumberFields(boolean value)](#setUnlinkPagesNumberFields-boolean) | 指定是否在生成的文档中将 NUMPAGES 字段替换为其实际的结果值。 |
| [setUpdatePageStartingNumber(boolean value)](#setUpdatePageStartingNumber-boolean) | 指定是否在生成的文档中更新起始页码。 |
### PageExtractOptions() {#PageExtractOptions}
```
public PageExtractOptions()
```


初始化此类的新实例。

### getUnlinkPagesNumberFields() {#getUnlinkPagesNumberFields}
```
public boolean getUnlinkPagesNumberFields()
```


指定是否在生成的文档中将 NUMPAGES 字段替换为其实际的结果值。默认值为 true。

 **Examples:** 

展示如何重置初始页码并保存 NUMPAGE 字段。

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
boolean - 相应的 boolean 值。
### getUpdatePageStartingNumber() {#getUpdatePageStartingNumber}
```
public boolean getUpdatePageStartingNumber()
```


指定是否在生成的文档中更新起始页码。默认值为 true。

 **Examples:** 

展示如何重置初始页码并保存 NUMPAGE 字段。

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
boolean - 相应的 boolean 值。
### setUnlinkPagesNumberFields(boolean value) {#setUnlinkPagesNumberFields-boolean}
```
public void setUnlinkPagesNumberFields(boolean value)
```


指定是否在生成的文档中将 NUMPAGES 字段替换为其实际的结果值。默认值为 true。

 **Examples:** 

展示如何重置初始页码并保存 NUMPAGE 字段。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

### setUpdatePageStartingNumber(boolean value) {#setUpdatePageStartingNumber-boolean}
```
public void setUpdatePageStartingNumber(boolean value)
```


指定是否在生成的文档中更新起始页码。默认值为 true。

 **Examples:** 

展示如何重置初始页码并保存 NUMPAGE 字段。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

