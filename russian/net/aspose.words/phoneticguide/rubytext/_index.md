---
title: PhoneticGuide.RubyText
second_title: Справочник по API Aspose.Words для .NET
description: PhoneticGuide свойство. Получает рубиновый текст фонетического руководства.
type: docs
weight: 20
url: /ru/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Получает рубиновый текст фонетического руководства.

```csharp
public string RubyText { get; }
```

### Примеры

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

* class [PhoneticGuide](../)
* пространство имен [Aspose.Words](../../phoneticguide/)
* сборка [Aspose.Words](../../../)


