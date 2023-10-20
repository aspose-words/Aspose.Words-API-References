---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: 用于 .NET 的 Aspose.Words
description: PageSet 构造函数. 根据精确的页面索引创建一页集 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

根据精确的页面索引创建一页集。

```csharp
public PageSet(int page)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| page | Int32 | 页面的从零开始的索引。 |

## 评论

如果遇到不在文档中的页面，渲染时会抛出异常。 MaxValue表示文档中的最后一页。

### 也可以看看

* class [PageSet](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

根据准确的页面索引创建页面集。

```csharp
public PageSet(params int[] pages)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pages | Int32[] | 从零开始的页面索引。 |

## 评论

如果遇到不在文档中的页面，渲染时会抛出异常。 MaxValue表示文档中的最后一页。

## 例子

展示如何根据准确的页面索引提取页面。

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
// 修改该方法如何将文档转换为 .XPS。
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// 使用“PageSet”属性选择一组文档页面以保存到输出 XPS。
// 在这种情况下，我们将通过从零开始的索引仅选择三个页面：第 1 页、第 2 页和第 4 页。
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### 也可以看看

* class [PageSet](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

基于范围创建页面集。

```csharp
public PageSet(params PageRange[] ranges)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ranges | PageRange[] | 页面范围数组。 |

## 评论

如果遇到从文档最后一页开始的范围， 在渲染过程中会抛出异常。 所有在最后一页之后结束的范围都会被截断以适应文档。

## 例子

显示如何根据确切的页面范围提取页面。

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
