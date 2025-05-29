---
title: SvgSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words for .NET
description: 探索 SvgSaveOptions IdPrefix 属性，它可以自定义输出文档中的元素 ID，从而实现更清晰的组织和显示效果。立即优化您的 SVG 文件！
type: docs
weight: 40
url: /zh/net/aspose.words.saving/svgsaveoptions/idprefix/
---
## SvgSaveOptions.IdPrefix property

指定在输出文档中所有生成的元素 ID 前面添加的前缀。 默认值为空，不添加任何前缀。

```csharp
public string IdPrefix { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentException | 该值不符合上面指定的要求。 |

## 评论

如果指定了前缀，则它只能包含字母、数字、下划线和连字符， 并且必须以字母开头。

## 例子

展示如何添加前缀到所有生成的元素 ID（svg）。

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

### 也可以看看

* class [SvgSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
