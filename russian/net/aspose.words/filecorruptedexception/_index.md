---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words для .NET
description: Aspose.Words.FileCorruptedException сорт. Выдается во время загрузки документа когда документ кажется поврежденным и его невозможно загрузить на С#.
type: docs
weight: 2800
url: /ru/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Выдается во время загрузки документа, когда документ кажется поврежденным и его невозможно загрузить.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) статья документации.

```csharp
public class FileCorruptedException : Exception
```

## Примеры

Показывает, как перехватить FileCorruptedException.

```csharp
try
{
    // Если мы получим сообщение об ошибке «Нечитаемое содержимое» при попытке открыть документ с помощью Microsoft Word,
    // есть вероятность, что мы получим исключение при попытке загрузить этот документ с помощью Aspose.Words.
    Document doc = new Document(MyDir + "Corrupted document.docx");
}
catch (FileCorruptedException e)
{
    Console.WriteLine(e.Message);
}
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
