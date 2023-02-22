---
title: ParagraphFormat.SnapToGrid
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Указывает должен ли текущий абзац использовать настройки линий сетки документа на странице при расположении содержимого в абзаце.
type: docs
weight: 280
url: /ru/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Указывает, должен ли текущий абзац использовать настройки линий сетки документа на странице при расположении содержимого в абзаце.

```csharp
public bool SnapToGrid { get; set; }
```

### Примеры

Показывает, как указать ограничение на количество строк, которые может иметь каждая страница.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Включите питчинг, а затем используйте его, чтобы установить количество строк на странице в этом разделе.
// Достаточно большой размер шрифта переместит несколько строк на следующую страницу, чтобы избежать перекрытия символов.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


