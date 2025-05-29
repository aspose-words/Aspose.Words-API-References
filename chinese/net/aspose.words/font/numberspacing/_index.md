---
title: Font.NumberSpacing
linktitle: NumberSpacing
articleTitle: NumberSpacing
second_title: Aspose.Words for .NET
description: 探索字体 NumberSpacing 属性，自定义数字间距，提升可读性和设计感。立即优化您的排版！
type: docs
weight: 290
url: /zh/net/aspose.words/font/numberspacing/
---
## Font.NumberSpacing property

获取或设置所显示数字的间距类型。

```csharp
public NumSpacing NumberSpacing { get; set; }
```

## 例子

展示如何设置数字的间距类型。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 此效果仅在较新版本的 MS Word 中受支持。
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### 也可以看看

* enum [NumSpacing](../../numspacing/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
