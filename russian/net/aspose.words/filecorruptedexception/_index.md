---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.FileCorruptedException, разработанный для легкой обработки поврежденных документов во время загрузки. Обеспечьте бесперебойное управление документами!
type: docs
weight: 3210
url: /ru/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Возникает во время загрузки документа, когда документ кажется поврежденным и его невозможно загрузить.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) документальная статья.

```csharp
public class FileCorruptedException : Exception
```

## Примеры

Показывает, как перехватить исключение FileCorruptedException.

```csharp
try
{
    // Если при попытке открыть документ с помощью Microsoft Word мы получаем сообщение об ошибке «Нечитаемое содержимое»,
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
