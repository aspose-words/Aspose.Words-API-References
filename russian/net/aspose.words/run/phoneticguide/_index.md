---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words для .NET
description: Откройте для себя безупречное произношение с PhoneticGuide. Улучшите свои языковые навыки и общение, получив доступ к персонализированным фонетическим подсказкам.
type: docs
weight: 40
url: /ru/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Получает`PhoneticGuide` объект.

```csharp
public PhoneticGuide PhoneticGuide { get; }
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

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
