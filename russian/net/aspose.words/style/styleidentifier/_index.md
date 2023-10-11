---
title: Style.StyleIdentifier
second_title: Справочник по API Aspose.Words для .NET
description: Style свойство. Получает независимый от локали идентификатор стиля для встроенного стиля.
type: docs
weight: 160
url: /ru/net/aspose.words/style/styleidentifier/
---
## Style.StyleIdentifier property

Получает независимый от локали идентификатор стиля для встроенного стиля.

```csharp
public StyleIdentifier StyleIdentifier { get; }
```

### Примечания

Для пользовательских (пользовательских) стилей это свойство возвращаетUser.

### Примеры

Показывает, как изменить положение правой позиции табуляции в абзацах, связанных с содержанием.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Перебираем все абзацы со стилями на основе результатов оглавления; это любой стиль между TOC и TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Получаем первую вкладку, используемую в этом абзаце. Это должна быть вкладка, используемая для выравнивания номеров страниц.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Заменяем первую табуляцию по умолчанию, остановку на пользовательскую позицию табуляции.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Смотрите также

* enum [StyleIdentifier](../../styleidentifier/)
* class [Style](../)
* пространство имен [Aspose.Words](../../style/)
* сборка [Aspose.Words](../../../)


