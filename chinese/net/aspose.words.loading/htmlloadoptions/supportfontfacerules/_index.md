---
title: HtmlLoadOptions.SupportFontFaceRules
linktitle: SupportFontFaceRules
articleTitle: SupportFontFaceRules
second_title: Aspose.Words for .NET
description: 探索 HtmlLoadOptions SupportFontFaceRules，轻松控制字体加载。启用自定义字体，打造更精致的网页设计。
type: docs
weight: 60
url: /zh/net/aspose.words.loading/htmlloadoptions/supportfontfacerules/
---
## HtmlLoadOptions.SupportFontFaceRules property

获取或设置一个值，指示是否支持@font-face 规则以及是否加载声明的字体。 默认值为`错误的`.

```csharp
public bool SupportFontFaceRules { get; set; }
```

## 评论

如果启用此选项，则会加载@font-face 规则中声明的字体并将其嵌入到结果文档的 字体定义中（请参阅[`FontInfos`](../../../aspose.words/documentbase/fontinfos/)）。这使得加载的字体可用于渲染，但 不会在保存时自动启用字体嵌入。为了保存已加载字体的文档， [`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/)的财产[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) 集合应设置为`真的`.

支持的字体格式为 TTF、EOT 和 WOFF。

加载 SVG 图像时不支持 @font-face 规则。

## 例子

展示如何加载声明的“@font-face”规则。

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();
loadOptions.SupportFontFaceRules = true;
Document doc = new Document(MyDir + "Html with FontFace.html", loadOptions);

Assert.AreEqual("Squarish Sans CT Regular", doc.FontInfos[0].Name);
```

### 也可以看看

* class [HtmlLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
