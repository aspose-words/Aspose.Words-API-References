---
title: LayoutOptions.ShowHiddenText
second_title: Aspose.Words for .NET API 参考
description: LayoutOptions 财产. 获取或设置是否呈现文档中隐藏文本的指示 默认为错误的.
type: docs
weight: 80
url: /zh/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

获取或设置是否呈现文档中隐藏文本的指示。 默认为`错误的`.

```csharp
public bool ShowHiddenText { get; set; }
```

### 评论

此属性影响所有隐藏内容，而不仅仅是文本。

### 例子

演示如何在渲染的输出文档中隐藏文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// 插入隐藏文本，然后指定我们是否希望从呈现的文档中省略它。
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### 也可以看看

* class [LayoutOptions](../)
* 命名空间 [Aspose.Words.Layout](../../layoutoptions/)
* 部件 [Aspose.Words](../../../)


