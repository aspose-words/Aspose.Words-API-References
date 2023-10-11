---
title: TxtSaveOptions.SimplifyListLabels
second_title: Aspose.Words for .NET API 参考
description: TxtSaveOptions 财产. 指定程序是否应在 复杂标签格式无法用纯文本充分表示的情况下简化列表标签
type: docs
weight: 70
url: /zh/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

指定程序是否应在 复杂标签格式无法用纯文本充分表示的情况下简化列表标签。

如果设置为`真的` ，编号列表标签以简单数字格式 书写，逐项列表标签以简单ASCII字符书写。默认值为`错误的`。

```csharp
public bool SimplifyListLabels { get; set; }
```

### 例子

演示如何在将文档保存为纯文本时更改列表的外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建具有五级缩进的项目符号列表。
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
// 将符号转换为更简单的 ASCII 字符，例如 '*'、'o'、'+'、'>' 等
// 将“SimplifyListLabels”属性设置为“false”以保留尽可能多的原始列表符号。
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

if (simplifyListLabels)
    Assert.AreEqual("* Item 1\r\n" +
                    "  > Item 2\r\n" +
                    "    + Item 3\r\n" +
                    "      - Item 4\r\n" +
                    "        o Item 5\r\n", docText);
else
    Assert.AreEqual("· Item 1\r\n" +
                    "o Item 2\r\n" +
                    "§ Item 3\r\n" +
                    "· Item 4\r\n" +
                    "o Item 5\r\n", docText);
```

### 也可以看看

* class [TxtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../txtsaveoptions/)
* 部件 [Aspose.Words](../../../)


