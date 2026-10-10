---
title: "AdvancedCompareOptions"
linktitle: "AdvancedCompareOptions"
second_title: "Aspose.Words for Java"
description: "允许在 Java 中设置高级比较选项。"
type: docs
weight: 13
url: /zh/java/com.aspose.words/advancedcompareoptions/
---

**Inheritance:**
java.lang.Object
```
public class AdvancedCompareOptions
```

允许设置高级比较选项。

 **Remarks:** 

这些选项在 Microsoft Word 中没有对应项，可能有助于生成更精确的比较结果。

 **Examples:** 

展示如何比较内容相同但存储项 ID 不同的 SDT。

```

 Document docA = new Document(getMyDir() + "Document with SDT 1.docx");
 Document docB = new Document(getMyDir() + "Document with SDT 2.docx");

 // Configure options to compare SDT with same content but different store item id.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreStoreItemId(false);

 docA.compare(docB, "user", new Date(), compareOptions);
 Assert.assertEquals(8, docA.getRevisions().getCount());

 compareOptions.getAdvancedOptions().setIgnoreStoreItemId(true);

 docA.getRevisions().rejectAll();
 docA.compare(docB, "user", new Date(), compareOptions);
 Assert.assertEquals(0, docA.getRevisions().getCount());
 
```
## 方法

| 方法 | 描述 |
| --- | --- |
| [getIgnoreDmlUniqueId()](#getIgnoreDmlUniqueId) | 指定是否忽略 DrawingML 唯一 Id 的差异。 |
| [getIgnoreStoreItemId()](#getIgnoreStoreItemId) | 指定是否忽略 StructuredDocumentTag 存储项 Id 的差异。 |
| [setIgnoreDmlUniqueId(boolean value)](#setIgnoreDmlUniqueId-boolean) | 指定是否忽略 DrawingML 唯一 Id 的差异。 |
| [setIgnoreStoreItemId(boolean value)](#setIgnoreStoreItemId-boolean) | 指定是否忽略 StructuredDocumentTag 存储项 Id 的差异。 |
### getIgnoreDmlUniqueId() {#getIgnoreDmlUniqueId}
```
public boolean getIgnoreDmlUniqueId()
```


指定是否忽略 DrawingML 唯一 Id 的差异。

 **Remarks:** 

默认值为 false。

 **Examples:** 

展示如何在比较文档时忽略 DML 唯一 ID。

```

 Document docA = new Document(getMyDir() + "DML unique ID original.docx");
 Document docB = new Document(getMyDir() + "DML unique ID compare.docx");

 // By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
 // If we are ignoring DML's unique ID, and revisions count were 0.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreDmlUniqueId(isIgnoreDmlUniqueId);

 docA.compare(docB, "Aspose.Words", new Date(), compareOptions);

 Assert.assertEquals(isIgnoreDmlUniqueId ? 1 : 3, docA.getRevisions().getCount());
 
```

**Returns:**
boolean - 相应的 boolean 值。
### getIgnoreStoreItemId() {#getIgnoreStoreItemId}
```
public boolean getIgnoreStoreItemId()
```


指定是否忽略 StructuredDocumentTag 存储项 Id 的差异。

 **Remarks:** 

默认值为 false。

 **Examples:** 

展示如何比较内容相同但存储项 ID 不同的 SDT。

```

 Document docA = new Document(getMyDir() + "Document with SDT 1.docx");
 Document docB = new Document(getMyDir() + "Document with SDT 2.docx");

 // Configure options to compare SDT with same content but different store item id.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreStoreItemId(false);

 docA.compare(docB, "user", new Date(), compareOptions);
 Assert.assertEquals(8, docA.getRevisions().getCount());

 compareOptions.getAdvancedOptions().setIgnoreStoreItemId(true);

 docA.getRevisions().rejectAll();
 docA.compare(docB, "user", new Date(), compareOptions);
 Assert.assertEquals(0, docA.getRevisions().getCount());
 
```

**Returns:**
boolean - 相应的 boolean 值。
### setIgnoreDmlUniqueId(boolean value) {#setIgnoreDmlUniqueId-boolean}
```
public void setIgnoreDmlUniqueId(boolean value)
```


指定是否忽略 DrawingML 唯一 Id 的差异。

 **Remarks:** 

默认值为 false。

 **Examples:** 

展示如何在比较文档时忽略 DML 唯一 ID。

```

 Document docA = new Document(getMyDir() + "DML unique ID original.docx");
 Document docB = new Document(getMyDir() + "DML unique ID compare.docx");

 // By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
 // If we are ignoring DML's unique ID, and revisions count were 0.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreDmlUniqueId(isIgnoreDmlUniqueId);

 docA.compare(docB, "Aspose.Words", new Date(), compareOptions);

 Assert.assertEquals(isIgnoreDmlUniqueId ? 1 : 3, docA.getRevisions().getCount());
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

### setIgnoreStoreItemId(boolean value) {#setIgnoreStoreItemId-boolean}
```
public void setIgnoreStoreItemId(boolean value)
```


指定是否忽略 StructuredDocumentTag 存储项 Id 的差异。

 **Remarks:** 

默认值为 false。

 **Examples:** 

展示如何比较内容相同但存储项 ID 不同的 SDT。

```

 Document docA = new Document(getMyDir() + "Document with SDT 1.docx");
 Document docB = new Document(getMyDir() + "Document with SDT 2.docx");

 // Configure options to compare SDT with same content but different store item id.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.getAdvancedOptions().setIgnoreStoreItemId(false);

 docA.compare(docB, "user", new Date(), compareOptions);
 Assert.assertEquals(8, docA.getRevisions().getCount());

 compareOptions.getAdvancedOptions().setIgnoreStoreItemId(true);

 docA.getRevisions().rejectAll();
 docA.compare(docB, "user", new Date(), compareOptions);
 Assert.assertEquals(0, docA.getRevisions().getCount());
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

