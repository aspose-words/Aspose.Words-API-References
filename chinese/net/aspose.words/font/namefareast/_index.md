---
title: Font.NameFarEast
linktitle: NameFarEast
articleTitle: NameFarEast
second_title: Aspose.Words for .NET
description: 发现 Font NameFarEast 属性，轻松自定义和设置东亚字体名称，以增强项目中的排版效果。
type: docs
weight: 260
url: /zh/net/aspose.words/font/namefareast/
---
## Font.NameFarEast property

返回或设置东亚字体名称。

```csharp
public string NameFarEast { get; set; }
```

## 例子

展示如何插入和格式化远东语言的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定文档构建器将应用于其插入的任何文本的字体设置。
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// 将我们的字体和语言环境命名为“FarEast”。
// 如果构建器使用此字体配置插入亚洲字符，则每次运行都会包含
// 这些字符将使用“FarEast”字体/语言环境而不是默认字体/语言环境来显示。
// 当西方字体无法理想地表示亚洲字符时，这可能会很有用。
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// 此文本将以默认字体/语言环境显示。
builder.Writeln("Hello world!");

// 由于这些是亚洲字符，因此本次运行将应用我们的“FarEast”字体/语言环境等效项。
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### 也可以看看

* property [Name](../name/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
