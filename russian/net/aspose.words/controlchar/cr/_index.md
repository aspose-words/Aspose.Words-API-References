---
title: ControlChar.Cr
linktitle: Cr
articleTitle: Cr
second_title: Aspose.Words для .NET
description: Откройте для себя ControlChar Cr, символ возврата каретки (x000d или r), который улучшает форматирование текста. Упростите кодирование с помощью наших уникальных решений!
type: docs
weight: 50
url: /ru/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

Символ возврата каретки: "\x000d" или "\r". То же, что и[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

## Примеры

Показывает, как использовать управляющие символы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте абзацы с текстом с помощью DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Преобразование документа в текстовую форму показывает, что управляющие символы
// представляют некоторые структурные элементы документа, такие как разрывы страниц.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// При преобразовании документа в строковую форму,
// мы можем опустить некоторые управляющие символы с помощью метода Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Смотрите также

* class [ControlChar](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
