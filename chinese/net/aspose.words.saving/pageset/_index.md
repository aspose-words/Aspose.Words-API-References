---
title: PageSet Class
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.PageSet 类，实现高效的文档管理。轻松定义随机页面集，提升您的工作流程！
type: docs
weight: 6170
url: /zh/net/aspose.words.saving/pageset/
---
## PageSet class

描述一组随机的页面。

要了解更多信息，请访问[使用文档进行编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public sealed class PageSet : IEnumerable<int>
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [PageSet](pageset/#constructor_1)(*int*) | 根据精确页面索引创建单页集。 |
| [PageSet](pageset/#constructor_2)(*params int[]*) | 根据精确的页面索引创建页面集。 |
| [PageSet](pageset/#constructor)(*params PageRange[]*) | 根据范围创建页面集。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| static [All](../../aspose.words.saving/pageset/all/) { get; } | 获取文档所有页面按原始顺序排列的集合。 |
| static [Even](../../aspose.words.saving/pageset/even/) { get; } | 获取文档所有偶数页按原始顺序排列的集合。 |
| static [Odd](../../aspose.words.saving/pageset/odd/) { get; } | 获取文档所有奇数页按原始顺序排列的集合。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEnumerator](../../aspose.words.saving/pageset/getenumerator/)() |  |

## 例子

展示如何将文档中的一页渲染为 JPEG 图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// 将“PageSet”设置为“1”以通过以下方式选择第二页
// 从零开始的索引来呈现文档。
options.PageSet = new PageSet(1);

// 当我们将文档保存为 JPEG 格式时，Aspose.Words 只会呈现一页。
// 此图像将包含从第二页开始的一页，
// 这只是原始文档的第二页。
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
