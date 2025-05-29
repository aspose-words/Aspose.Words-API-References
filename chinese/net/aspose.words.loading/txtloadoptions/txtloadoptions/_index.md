---
title: TxtLoadOptions
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words for .NET
description: 探索 TxtLoadOptions 构造函数！轻松使用默认值进行初始化，并简化数据加载流程，从而提升性能。
type: docs
weight: 10
url: /zh/net/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions constructor

使用默认值初始化此类的新实例。

```csharp
public TxtLoadOptions()
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
