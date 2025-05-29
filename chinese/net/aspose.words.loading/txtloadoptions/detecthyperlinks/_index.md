---
title: TxtLoadOptions.DetectHyperlinks
linktitle: DetectHyperlinks
articleTitle: DetectHyperlinks
second_title: Aspose.Words for .NET
description: 了解 TxtLoadOptions 的 DetectHyperlinks 属性如何通过检测超链接来增强文本处理，从而提高数据准确性。默认值为 false。
type: docs
weight: 30
url: /zh/net/aspose.words.loading/txtloadoptions/detecthyperlinks/
---
## TxtLoadOptions.DetectHyperlinks property

指定检测文本中的超链接。 默认值为`错误的`.

```csharp
public bool DetectHyperlinks { get; set; }
```

## 例子

展示如何读取和显示超链接。

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n”；

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // 加载带有超链接的文档。
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // 打印超链接文本。
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/”);
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/”);
}
```

### 也可以看看

* class [TxtLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
