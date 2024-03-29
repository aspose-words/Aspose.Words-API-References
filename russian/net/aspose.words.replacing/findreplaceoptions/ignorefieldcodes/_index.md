---
title: FindReplaceOptions.IgnoreFieldCodes
linktitle: IgnoreFieldCodes
articleTitle: IgnoreFieldCodes
second_title: Aspose.Words для .NET
description: FindReplaceOptions IgnoreFieldCodes свойство. Получает или задает логическое значение указывающее следует ли игнорировать текст внутри кодов полей. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 70
url: /ru/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри кодов полей. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IgnoreFieldCodes { get; set; }
```

## Примечания

Эта опция влияет только на коды полей (она не игнорирует узлы между FieldSeparator иFieldEnd).

Чтобы игнорировать все поле, используйте соответствующую опцию[`IgnoreFields`](../ignorefields/).

## Примеры

Показывает, как игнорировать текст внутри кодов полей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// Заменить 'T' в документе, игнорируя текст внутри кода поля или нет.
doc.Range.Replace(new Regex("T"), "*", options);
Console.WriteLine(doc.GetText());

Assert.AreEqual(
    ignoreFieldCodes
        ? "\u0013INCLUDETEXT\u0014*est I*!\u0015"
        : "\u0013INCLUDE*EX*\u0014*est I*!\u0015", doc.GetText().Trim());
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
