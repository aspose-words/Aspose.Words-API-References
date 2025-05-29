---
title: ParagraphFormat.SnapToGrid
linktitle: SnapToGrid
articleTitle: SnapToGrid
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ParagraphFormat SnapToGrid повышает точность макета, выравнивая абзацы по линиям сетки документа, что придает ему изысканный вид.
type: docs
weight: 300
url: /ru/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Указывает, должен ли текущий абзац использовать линии сетки документа на страницу settings при размещении содержимого в абзаце.

```csharp
public bool SnapToGrid { get; set; }
```

## Примеры

Показывает, как указать ограничение на количество строк на каждой странице.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Включите питч, а затем используйте его для установки количества строк на странице в этом разделе.
// Достаточно большой размер шрифта сдвинет некоторые строки на следующую страницу, чтобы избежать перекрытия символов.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
