---
title: FontSourceBase.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words for .NET
description: 探索 FontSourceBase Priority 属性，优化您的字体来源。轻松提升性能并改善用户体验！
type: docs
weight: 10
url: /zh/net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

返回字体源优先级。

```csharp
public int Priority { get; }
```

## 评论

当不同字体源中存在具有相同系列名称和样式的字体时使用此值。 在这种情况下，Aspose.Words 从具有较高优先级值的源中选择字体。

默认值为 0。

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

* class [FontSourceBase](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
