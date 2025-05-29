---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.FileCorruptedException 类，它旨在轻松处理加载过程中损坏的文档。确保无缝文档管理！
type: docs
weight: 3210
url: /zh/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

在文档加载期间抛出，当文档似乎已损坏且无法加载时。

要了解更多信息，请访问[使用文档进行编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public class FileCorruptedException : Exception
```

## 例子

展示如何捕获 FileCorruptedException。

```csharp
try
{
    // 如果我们在尝试使用 Microsoft Word 打开文档时收到“无法读取内容”错误消息，
    // 当我们尝试使用 Aspose.Words 加载该文档时，很可能会抛出异常。
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
