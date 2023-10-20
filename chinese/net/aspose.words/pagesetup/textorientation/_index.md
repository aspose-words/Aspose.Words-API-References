---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: 用于 .NET 的 Aspose.Words
description: PageSetup TextOrientation 财产. 允许指定TextOrientation对于整个页面 默认值为Horizontal 在 C#.
type: docs
weight: 430
url: /zh/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

允许指定`TextOrientation`对于整个页面。 默认值为Horizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## 评论

此属性仅支持 MS Word 本机格式 DOCX、WML、RTF 和 DOC。

## 例子

显示如何设置文本方向。

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 将“TextOrientation”属性设置为“TextOrientation.Upward”，将所有文本旋转 90 度
// 向右，这样所有从左到右的文本现在都是从上到下的。
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### 也可以看看

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
