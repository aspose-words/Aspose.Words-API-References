---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: Aspose.Words для .NET
description: Управляйте переносами в документе с помощью свойства ParagraphFormat SuppressAutoHyphens, обеспечивая четкое и профессиональное форматирование абзацев.
type: docs
weight: 380
url: /ru/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Указывает, следует ли освободить текущий абзац от любых переносов, которые применяются в настройках документа.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## Примеры

Показывает, как подавить переносы в абзаце.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Открываем документ, содержащий текст с локалью, соответствующей локали нашего словаря.
// При сохранении этого документа в формате сохранения с фиксированным размером страницы его текст будет иметь переносы.
Document doc = new Document(MyDir + "German text.docx");

// Мы можем установить свойство "SuppressAutoHyphens" в значение "true", чтобы отключить переносы
// для определенного абзаца, сохраняя его включенным для остальной части документа.
// Значение по умолчанию для этого свойства — «false»,
// что означает, что в каждом абзаце по умолчанию используются переносы, если таковые имеются.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
