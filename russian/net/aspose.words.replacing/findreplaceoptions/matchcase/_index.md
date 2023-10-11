---
title: FindReplaceOptions.MatchCase
second_title: Справочник по API Aspose.Words для .NET
description: FindReplaceOptions свойство. True указывает на сравнение с учетом регистра false указывает на сравнение без учета регистра.
type: docs
weight: 140
url: /ru/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

True указывает на сравнение с учетом регистра, false указывает на сравнение без учета регистра.

```csharp
public bool MatchCase { get; set; }
```

### Примеры

Показывает, как переключить чувствительность к регистру при выполнении операции поиска и замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите для флага «MatchCase» значение «true», чтобы применять чувствительность к регистру при поиске заменяемых строк.
// Установите флаг «MatchCase» в значение «false», чтобы игнорировать регистр символов при поиске текста для замены.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../findreplaceoptions/)
* сборка [Aspose.Words](../../../)


