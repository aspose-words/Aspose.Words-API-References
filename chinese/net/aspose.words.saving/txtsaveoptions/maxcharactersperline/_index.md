---
title: TxtSaveOptions.MaxCharactersPerLine
second_title: Aspose.Words for .NET API 参考
description: TxtSaveOptions 财产. 获取或设置一个整数值指定每一行的最大字符数 默认值为 0表示没有限制
type: docs
weight: 40
url: /zh/net/aspose.words.saving/txtsaveoptions/maxcharactersperline/
---
## TxtSaveOptions.MaxCharactersPerLine property

获取或设置一个整数值，指定每一行的最大字符数。 默认值为 0，表示没有限制。

```csharp
public int MaxCharactersPerLine { get; set; }
```

### 例子

演示如何设置每行的最大字符数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// 将每一行允许的最大字符数设置为 30 个。
TxtSaveOptions saveOptions = new TxtSaveOptions { MaxCharactersPerLine = 30 };

doc.Save(ArtifactsDir + "TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

### 也可以看看

* class [TxtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../txtsaveoptions/)
* 部件 [Aspose.Words](../../../)


