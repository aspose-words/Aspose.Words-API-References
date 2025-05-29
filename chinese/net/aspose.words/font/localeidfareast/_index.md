---
title: Font.LocaleIdFarEast
linktitle: LocaleIdFarEast
articleTitle: LocaleIdFarEast
second_title: Aspose.Words for .NET
description: 探索 Font LocaleIdFarEast 属性，轻松管理格式化亚洲字符的区域设置标识符，增强您的多语言应用程序。
type: docs
weight: 220
url: /zh/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

获取或设置格式化亚洲字符的区域设置标识符（语言）。

```csharp
public int LocaleIdFarEast { get; set; }
```

## 评论

有关区域标识符列表，请参阅 https://msdn.microsoft.com/en-us/library/cc233965.aspx

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

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
