---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PhoneticGuide BaseText, чтобы легко получать доступ к базовому тексту фонетического руководства и улучшать его для повышения ясности и коммуникативности.
type: docs
weight: 10
url: /ru/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

Получает базовый текст фонетического руководства.

```csharp
public string BaseText { get; }
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
