---
title: FileFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: 探索 FileFontSource Type 属性以轻松识别字体源类型，并通过精确的排版解决方案增强您的设计项目。
type: docs
weight: 40
url: /zh/net/aspose.words.fonts/filefontsource/type/
---
## FileFontSource.Type property

返回字体源的类型。

```csharp
public override FontSourceType Type { get; }
```

## 例子

展示如何使用本地文件系统中的字体文件作为字体源。

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### 也可以看看

* enum [FontSourceType](../../fontsourcetype/)
* class [FileFontSource](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
