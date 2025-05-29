---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words for .NET
description: 使用 PageSet 构造函数轻松创建定制的单页集，旨在实现精确的页面索引和无缝的用户体验。
type: docs
weight: 10
url: /zh/net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

根据精确页面索引创建单页集。

```csharp
public PageSet(int page)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| page | Int32 | 页面的从零开始的索引。 |

## 评论

如果遇到不在文档中的页面，则在渲染过程中会抛出异常。 MaxValue表示文档的最后一页。

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

* class [PageSet](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

根据精确的页面索引创建页面集。

```csharp
public PageSet(params int[] pages)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pages | Int32[] | 页面的零基索引。 |

## 评论

如果遇到不在文档中的页面，则在渲染过程中会抛出异常。 MaxValue表示文档的最后一页。

## 例子

展示如何根据精确的页面索引提取页面。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 向文档添加五页。
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// 创建一个“XpsSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .XPS 的方式。
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// 使用“PageSet”属性选择一组文档页面来保存到输出 XPS。
// 在这种情况下，我们将通过从零开始的索引仅选择三页：第 1 页、第 2 页和第 4 页。
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### 也可以看看

* class [PageSet](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

根据范围创建页面集。

```csharp
public PageSet(params PageRange[] ranges)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ranges | PageRange[] | 页面范围数组。 |

## 评论

如果遇到从文档最后一页之后开始的范围， 则在渲染过程中会抛出异常。 所有在最后一页之后结束的范围都会被截断以适合文档。

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

* class [PageRange](../../pagerange/)
* class [PageSet](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
