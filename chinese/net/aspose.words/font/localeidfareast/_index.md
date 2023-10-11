---
title: Font.LocaleIdFarEast
second_title: Aspose.Words for .NET API 参考
description: Font 财产. 获取或设置格式化亚洲字符的区域设置标识符语言
type: docs
weight: 220
url: /zh/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

获取或设置格式化亚洲字符的区域设置标识符（语言）。

```csharp
public int LocaleIdFarEast { get; set; }
```

### 评论

有关区域设置标识符的列表，请参阅 https://msdn.microsoft.com/en-us/library/cc233965.aspx

### 例子

演示如何用远东语言插入文本并设置其格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 指定文档生成器将应用于其插入的任何文本的字体设置。
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// 为我们的字体和区域设置命名“FarEast”等效项。
// 如果构建器使用此字体配置插入亚洲字符，则每次运行都包含
// 这些字符将使用“FarEast”字体/区域设置而不是默认显示。
// 当西方字体没有亚洲字符的理想表示时，这可能很有用。
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// 此文本将以默认字体/区域设置显示。
builder.Writeln("Hello world!");

// 由于这些是亚洲字符，因此这次运行将应用我们的“FarEast”字体/区域设置等效项。
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../font/)
* 部件 [Aspose.Words](../../../)


