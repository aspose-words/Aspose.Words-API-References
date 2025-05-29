---
title: TxtLoadOptions
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор TxtLoadOptions! Простая инициализация со значениями по умолчанию и оптимизация процесса загрузки данных для повышения производительности.
type: docs
weight: 10
url: /ru/net/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions constructor

Инициализирует новый экземпляр этого класса со значениями по умолчанию.

```csharp
public TxtLoadOptions()
```

## Примеры

Показывает, как читать и отображать гиперссылки.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // Загрузить документ с гиперссылками.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Печать текста гиперссылки.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### Смотрите также

* class [TxtLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
