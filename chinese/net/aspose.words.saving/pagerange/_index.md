---
title: PageRange Class
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.PageRange 类，轻松定义连续的页面范围。提高文档处理的精确度和效率。
type: docs
weight: 6150
url: /zh/net/aspose.words.saving/pagerange/
---
## PageRange class

表示连续的页面范围。

要了解更多信息，请访问[使用文档进行编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public sealed class PageRange
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [PageRange](pagerange/)(*int, int*) | 创建一个新的页面范围对象。 |

## 例子

显示如何根据精确的页面范围提取页面。

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
