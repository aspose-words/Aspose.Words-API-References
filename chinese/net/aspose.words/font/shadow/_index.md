---
title: Font.Shadow
second_title: Aspose.Words for .NET API 参考
description: Font 财产. 如果字体被格式化为阴影则为真
type: docs
weight: 330
url: /zh/net/aspose.words/font/shadow/
---
## Font.Shadow property

如果字体被格式化为阴影，则为真。

```csharp
public bool Shadow { get; set; }
```

### 例子

展示如何创建一系列带有阴影格式的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 设置 Shadow 标志以应用偏移阴影效果，
// 使它看起来像字母漂浮在页面上方。
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../font/)
* 部件 [Aspose.Words](../../../)


