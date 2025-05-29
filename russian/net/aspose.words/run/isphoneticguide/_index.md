---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words для .NET
description: Откройте для себя IsPhoneticGuide — мощный инструмент, который определяет, служит ли строка фонетическим руководством, повышая ясность и читабельность вашего текста.
type: docs
weight: 20
url: /ru/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Возвращает логическое значение, указывающее, является ли прогон фонетическим руководством.

```csharp
public bool IsPhoneticGuide { get; }
```

## Примеры

Показывает, как получить свойства фонетического справочника.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Используйте фонетическое руководство в азиатском тексте.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### Смотрите также

* class [Run](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
