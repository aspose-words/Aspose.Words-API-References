---
title: TxtSaveOptionsBase.Encoding
second_title: Aspose.Words for .NET API 参考
description: TxtSaveOptionsBase 财产. 指定以文本格式导出时要使用的编码 默认值为 编码.UTF8.
type: docs
weight: 10
url: /zh/net/aspose.words.saving/txtsaveoptionsbase/encoding/
---
## TxtSaveOptionsBase.Encoding property

指定以文本格式导出时要使用的编码。 默认值为 **编码.UTF8**.

```csharp
public Encoding Encoding { get; set; }
```

### 例子

显示如何为 .txt 输出文档设置编码。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 添加一些包含 ASCII 字符集之外的字符的文本。
builder.Write("À È Ì Ò Ù.");

// 创建一个“TxtSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改我们如何将文档保存为纯文本。
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// 验证“Encoding”属性是否包含适合我们文档内容的编码。
Assert.AreEqual(System.Text.Encoding.UTF8, txtSaveOptions.Encoding);

doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

string docText = System.Text.Encoding.UTF8.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt"));

Assert.AreEqual("\uFEFFÀ È Ì Ò Ù.\r\n", docText);

// 使用不合适的编码可能会导致文档内容丢失。
txtSaveOptions.Encoding = System.Text.Encoding.ASCII;
doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System.Text.Encoding.ASCII.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt"));

Assert.AreEqual("? ? ? ? ?.\r\n", docText);
```

### 也可以看看

* class [TxtSaveOptionsBase](../)
* 命名空间 [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* 部件 [Aspose.Words](../../../)


