---
title: PhoneticGuide Class
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.PhoneticGuide для улучшения читаемости текста с фонетическими руководствами. Улучшите пользовательский опыт и доступность без усилий!
type: docs
weight: 5160
url: /ru/net/aspose.words/phoneticguide/
---
## PhoneticGuide class

Представляет фонетическое руководство.

```csharp
public class PhoneticGuide
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BaseText](../../aspose.words/phoneticguide/basetext/) { get; } | Получает базовый текст фонетического руководства. |
| [RubyText](../../aspose.words/phoneticguide/rubytext/) { get; } | Получает рубиновый текст фонетического руководства. |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
