---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words для .NET
description: Run PhoneticGuide свойство. ПолучаетPhoneticGuide объект на С#.
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
// Использование фонетического руководства в азиатском тексте.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### Смотрите также

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
