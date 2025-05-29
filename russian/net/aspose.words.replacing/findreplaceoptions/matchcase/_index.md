---
title: FindReplaceOptions.MatchCase
linktitle: MatchCase
articleTitle: MatchCase
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MatchCase в FindReplaceOptions, включите сравнение с учетом или без учета регистра для точного редактирования текста. Оптимизируйте свой рабочий процесс!
type: docs
weight: 140
url: /ru/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

True указывает на сравнение с учетом регистра, false указывает на сравнение без учета регистра.

```csharp
public bool MatchCase { get; set; }
```

## Примеры

Показывает, как включить чувствительность к регистру при выполнении операции поиска и замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите флаг «MatchCase» в значение «true», чтобы учитывать регистр при поиске строк для замены.
// Установите флаг «MatchCase» на «false», чтобы игнорировать регистр символов при поиске текста для замены.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
