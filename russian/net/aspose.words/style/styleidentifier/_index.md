---
title: StyleIdentifier
second_title: Справочник по API Aspose.Words для .NET
description: Получает независимый от языкового стандарта идентификатор стиля для встроенного стиля.
type: docs
weight: 140
url: /ru/net/aspose.words/style/styleidentifier/
---
## Style.StyleIdentifier property

Получает независимый от языкового стандарта идентификатор стиля для встроенного стиля.

```csharp
public StyleIdentifier StyleIdentifier { get; }
```

### Примечания

Для пользовательских (настраиваемых) стилей это свойство возвращаетUser.

### Примеры

Показывает, как изменить положение правой позиции табуляции в абзацах, связанных с оглавлением.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Итерация по всем абзацам со стилями оглавления на основе результатов; это любой стиль между TOC и TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Получите первую вкладку, используемую в этом абзаце, это должна быть вкладка, используемая для выравнивания номеров страниц.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Замените первую вкладку по умолчанию, остановку пользовательской остановкой табуляции.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Смотрите также

* enum [StyleIdentifier](../../styleidentifier)
* class [Style](../../style)
* пространство имен [Aspose.Words](../../style)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
