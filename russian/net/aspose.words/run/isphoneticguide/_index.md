---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words для .NET
description: Run IsPhoneticGuide свойство. Получает логическое значение указывающее является ли запуск фонетическим руководством на С#.
type: docs
weight: 20
url: /ru/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Получает логическое значение, указывающее, является ли запуск фонетическим руководством.

```csharp
public bool IsPhoneticGuide { get; }
```

## Примеры

Показывает, как получить свойства фонетического справочника.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");            

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Использование фонетического руководства в азиатском тексте.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### Смотрите также

* class [Run](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
