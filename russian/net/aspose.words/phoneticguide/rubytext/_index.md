---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PhoneticGuide RubyText для доступа к тексту Ruby и его улучшения с целью повышения фонетической ясности ваших приложений.
type: docs
weight: 20
url: /ru/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Получает рубиновый текст фонетического руководства.

```csharp
public string RubyText { get; }
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

* class [PhoneticGuide](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
