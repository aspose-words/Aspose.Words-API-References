---
title: "IDocumentMergerPlugin"
linktitle: "IDocumentMergerPlugin"
second_title: "Aspose.Words for Java"
description: "定义一个用于外部合并插件的接口，该插件可以在 Java 中合并 PDF 文档。"
type: docs
weight: 759
url: /zh/java/com.aspose.words/idocumentmergerplugin/
---
```
public interface IDocumentMergerPlugin
```

定义一个用于外部合并插件的接口，该插件可以合并 PDF 文档。
## 方法

| 方法 | 描述 |
| --- | --- |
| [merge(OutputStream outputStream, InputStream[] inputStreams, LoadOptions[] loadOptions)](#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.LoadOptions) |  |
### merge(OutputStream outputStream, InputStream[] inputStreams, LoadOptions[] loadOptions) {#merge-java.io.OutputStream-java.io.InputStream---com.aspose.words.LoadOptions}
```
public abstract void merge(OutputStream outputStream, InputStream[] inputStreams, LoadOptions[] loadOptions)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| inputStreams | java.io.InputStream[] |  |
| loadOptions | [LoadOptions\[\]](../../com.aspose.words/loadoptions/) |  |

