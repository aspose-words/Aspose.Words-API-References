---
title: Comparer.CompareToImages
linktitle: CompareToImages
articleTitle: CompareToImages
second_title: Aspose.Words for .NET
description: 使用 CompareToImages 轻松比较文档，将差异保存为每页的图像，增强清晰度和视觉分析。
type: docs
weight: 30
url: /zh/net/aspose.words.lowcode/comparer/comparetoimages/
---
## CompareToImages(*string, string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages_1}

比较两个文档并将差异保存为图像。 返回数组中的每个项目都代表以图像形式呈现的输出的单个页面。

```csharp
public static Stream[] CompareToImages(string v1, string v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| v1 | String | 原始文件。 |
| v2 | String | 修改后的文档。 |
| imageSaveOptions | ImageSaveOptions | 输出的图像保存选项。 |
| author | String | 用于修订的作者姓名首字母。 |
| dateTime | DateTime | 用于修订的日期和时间。 |
| compareOptions | CompareOptions | 文档比较选项。 |

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## CompareToImages(*Stream, Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages}

比较两个文档并将差异保存为图像。 返回数组中的每个项目都代表以图像形式呈现的输出的单个页面。

```csharp
public static Stream[] CompareToImages(Stream v1, Stream v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| v1 | Stream | 原始文件。 |
| v2 | Stream | 修改后的文档。 |
| imageSaveOptions | ImageSaveOptions | 输出的图像保存选项。 |
| author | String | 用于修订的作者姓名首字母。 |
| dateTime | DateTime | 用于修订的日期和时间。 |
| compareOptions | CompareOptions | 文档比较选项。 |

## 例子

展示如何比较文档并将结果保存为图像。

```csharp
// 有几种方法可以比较文档：
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Stream[] pages = Comparer.CompareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime());

using (FileStream firstStreamIn = new FileStream(firstDoc, FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(secondDoc, FileMode.Open, FileAccess.Read))
    {
        CompareOptions compareOptions = new CompareOptions();
        compareOptions.IgnoreCaseChanges = true;
        pages = Comparer.CompareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime(), compareOptions);
    }
}
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
