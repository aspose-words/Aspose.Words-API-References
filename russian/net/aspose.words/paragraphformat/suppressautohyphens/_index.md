---
title: ParagraphFormat.SuppressAutoHyphens
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Указывает следует ли освободить текущий абзац от любых переносов которые применяются в настройках документа.
type: docs
weight: 370
url: /ru/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Указывает, следует ли освободить текущий абзац от любых переносов, которые применяются в настройках документа.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

### Примеры

Показывает, как подавить переносы в абзаце.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Откройте документ, содержащий текст с локалью, соответствующей нашему словарю.
// Когда мы сохраняем этот документ в фиксированном формате страницы, в его тексте будут переносы.
Document doc = new Document(MyDir + "German text.docx");

// Мы можем установить для свойства «SuppressAutoHyphens» значение «true», чтобы отключить расстановку переносов.
// для определенного абзаца, сохраняя его включенным для остальной части документа.
// Значение по умолчанию для этого свойства — «false»,
// это означает, что каждый абзац по умолчанию использует переносы, если таковые имеются.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


