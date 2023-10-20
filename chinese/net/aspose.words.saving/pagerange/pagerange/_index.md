---
title: PageRange
linktitle: PageRange
articleTitle: PageRange
second_title: 用于 .NET 的 Aspose.Words
description: PageRange 构造函数. 创建一个新的页面范围对象 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.saving/pagerange/pagerange/
---
## PageRange constructor

创建一个新的页面范围对象。

```csharp
public PageRange(int from, int to)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| from | Int32 | 起始页从零开始的索引。 |
| to | Int32 | 结束页从零开始的索引。 如果它超出文档中最后一页的索引，则 将被截断以适合渲染时的文档。 |

## 评论

MaxValue表示文档中的最后一页。

## 例子

展示如何根据确切的页面范围提取页面。

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### 也可以看看

* class [PageRange](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
