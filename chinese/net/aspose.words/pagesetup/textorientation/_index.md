---
title: PageSetup.TextOrientation
second_title: Aspose.Words for .NET API 参考
description: PageSetup 财产. 允许指定TextOrientation整个页面 默认值为Horizontal
type: docs
weight: 430
url: /zh/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

允许指定`TextOrientation`整个页面。 默认值为Horizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

### 评论

仅 MS Word 本机格式 DOCX、WML、RTF 和 DOC 支持此属性。

### 例子

展示如何设置文本方向。

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// 将“TextOrientation”属性设置为“TextOrientation.Upward”，将所有文本旋转 90 度
// 向右，以便所有从左到右的文本现在从上到下。
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### 也可以看看

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../pagesetup/)
* 部件 [Aspose.Words](../../../)


