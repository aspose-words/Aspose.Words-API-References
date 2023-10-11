---
title: HyphenationOptions.HyphenateCaps
second_title: Aspose.Words for .NET API 参考
description: HyphenationOptions 财产. 获取或设置确定全部大写字母书写的单词是否连字符的值 此属性的默认值为真的.
type: docs
weight: 40
url: /zh/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

获取或设置确定全部大写字母书写的单词是否连字符的值。 此属性的默认值为`真的`.

```csharp
public bool HyphenateCaps { get; set; }
```

### 例子

展示如何配置自动连字。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### 也可以看看

* class [HyphenationOptions](../)
* 命名空间 [Aspose.Words.Settings](../../hyphenationoptions/)
* 部件 [Aspose.Words](../../../)


