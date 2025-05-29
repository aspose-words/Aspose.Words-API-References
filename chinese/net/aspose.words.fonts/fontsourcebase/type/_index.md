---
title: FontSourceBase.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: 发现 FontSourceBase 类型属性，轻松检索字体源类型以增强您的网页设计并优化用户体验。
type: docs
weight: 20
url: /zh/net/aspose.words.fonts/fontsourcebase/type/
---
## FontSourceBase.Type property

返回字体源的类型。

```csharp
public abstract FontSourceType Type { get; }
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
* class [FontSourceBase](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
