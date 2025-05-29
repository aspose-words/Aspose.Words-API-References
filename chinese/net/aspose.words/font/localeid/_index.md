---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words for .NET
description: 了解 Font LocaleId 属性如何通过管理不同字符语言的区域设置标识符来增强文本格式。立即提升您的编码水平！
type: docs
weight: 200
url: /zh/net/aspose.words/font/localeid/
---
## Font.LocaleId property

获取或设置格式化字符的区域标识符（语言）。

```csharp
public int LocaleId { get; set; }
```

## 评论

有关区域标识符列表，请参阅 https://msdn.microsoft.com/en-us/library/cc233965.aspx

## 例子

展示如何使用文档生成器设置我们添加的文本的语言环境。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 如果我们将字体的语言环境设置为英语并插入一些俄语文本，
// 英语区域拼写检查器将无法识别该文本并将其检测为拼写错误。
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// 为我们即将添加的文本设置匹配的语言环境，以应用适当的拼写检查器。
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
