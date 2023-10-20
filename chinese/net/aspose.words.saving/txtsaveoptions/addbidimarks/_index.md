---
title: TxtSaveOptions.AddBidiMarks
linktitle: AddBidiMarks
articleTitle: AddBidiMarks
second_title: 用于 .NET 的 Aspose.Words
description: TxtSaveOptions AddBidiMarks 财产. 指定以纯文本格式导出时是否在每次 BiDi 运行之前添加双向标记 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

指定以纯文本格式导出时是否在每次 BiDi 运行之前添加双向标记。

默认值为`错误的`。

```csharp
public bool AddBidiMarks { get; set; }
```

## 例子

演示如何在文本中的每个双向运行之前插入 Unicode 字符“从右到左标记”(U+200F)。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// 创建一个“TxtSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改我们将文档保存为纯文本的方式。
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// 将“AddBidiMarks”属性设置为“true”以在运行前添加标记
// 用从右到左的文本来指示事实。
// 将“AddBidiMarks”属性设置为“false”以从左到右写入
// 和从右到左的运行方式相同，没有任何内容来指示哪个是哪个。
saveOptions.AddBidiMarks = addBidiMarks;

doc.Save(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt", saveOptions);

string docText = System.Text.Encoding.Unicode.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    Assert.AreEqual("\uFEFFHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    Assert.True(docText.Contains("\u200f"));
}
else
{
    Assert.AreEqual("\uFEFFHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    Assert.False(docText.Contains("\u200f"));
}
```

### 也可以看看

* class [TxtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
