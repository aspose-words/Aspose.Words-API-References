---
title: HtmlFixedSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words for .NET
description: 探索 HtmlFixedSaveOptions IdPrefix 属性，自定义文档中的元素 ID。使用自定义前缀增强组织，获得更佳输出效果！
type: docs
weight: 100
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/idprefix/
---
## HtmlFixedSaveOptions.IdPrefix property

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

展示如何添加前缀到所有生成的元素 ID 之前。

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
