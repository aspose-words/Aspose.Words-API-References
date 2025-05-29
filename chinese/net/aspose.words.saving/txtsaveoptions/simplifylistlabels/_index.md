---
title: TxtSaveOptions.SimplifyListLabels
linktitle: SimplifyListLabels
articleTitle: SimplifyListLabels
second_title: Aspose.Words for .NET
description: 了解 TxtSaveOptions 的 SimplifyListLabels 功能如何通过简化复杂列表标签来改善文本表示，从而提高清晰度。
type: docs
weight: 70
url: /zh/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

指定程序是否应简化列表标签，以防万一复杂的标签格式无法用纯文本充分表示。

如果设置为`真的` ，编号列表标签以简单数字格式 书写，而逐项列表标签则以简单 ASCII 字符书写。默认值为`错误的`。

```csharp
public bool SimplifyListLabels { get; set; }
```

## 例子

展示如何在将文档保存为纯文本时更改列表的外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个具有五级缩进的项目符号列表。
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent();
builder.Writeln("Item 3");
builder.ListFormat.ListIndent();
builder.Writeln("Item 4");
builder.ListFormat.ListIndent();
builder.Write("Item 5");

// 创建一个“TxtSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改我们将文档保存为纯文本的方式。
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// 将“SimplifyListLabels”属性设置为“true”以转换某些列表
// 符号转换为更简单的 ASCII 字符，例如 '*'、'o'、'+'、'>' 等。
// 将“SimplifyListLabels”属性设置为“false”以保留尽可能多的原始列表符号。
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

string newLine = Environment.NewLine;

if (simplifyListLabels)
    Assert.AreEqual($"* Item 1{newLine}" +
                    $"  > Item 2{newLine}" +
                    $"    + Item 3{newLine}" +
                    $"      - Item 4{newLine}" +
                    $"        o Item 5{newLine}", docText);
else
    Assert.AreEqual($"· Item 1{newLine}" +
                    $"o Item 2{newLine}" +
                    $"§ Item 3{newLine}" +
                    $"· Item 4{newLine}" +
                    $"o Item 5{newLine}", docText);
```

### 也可以看看

* class [TxtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
