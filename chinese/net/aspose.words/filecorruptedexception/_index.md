---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.FileCorruptedException 班级. 在文档加载期间当文档似乎已损坏并且无法加载时抛出 在 C#.
type: docs
weight: 2800
url: /zh/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

在文档加载期间，当文档似乎已损坏并且无法加载时抛出。

要了解更多信息，请访问[使用文档编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public class FileCorruptedException : Exception
```

## 例子

演示如何捕获 FileCorruptedException。

```csharp
try
{
    // 如果我们在尝试使用 Microsoft Word 打开文档时收到“无法读取内容”错误消息，
    // 当尝试使用 Aspose.Words 加载该文档时，我们很可能会抛出异常。
    Document doc = new Document(MyDir + "Corrupted document.docx");
}
catch (FileCorruptedException e)
{
    Console.WriteLine(e.Message);
}
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
