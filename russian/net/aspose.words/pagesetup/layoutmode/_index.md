---
title: PageSetup.LayoutMode
linktitle: LayoutMode
articleTitle: LayoutMode
second_title: Aspose.Words для .NET
description: PageSetup LayoutMode свойство. Получает или задает режим макета этого раздела на С#.
type: docs
weight: 190
url: /ru/net/aspose.words/pagesetup/layoutmode/
---
## PageSetup.LayoutMode property

Получает или задает режим макета этого раздела.

```csharp
public SectionLayoutMode LayoutMode { get; set; }
```

## Примеры

Показывает, как указать количество символов, которое может иметь каждая строка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Включите шаг, а затем используйте его, чтобы установить количество символов в строке в этом разделе.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Количество символов также зависит от размера шрифта.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

Показывает, как указать ограничение на количество строк, которое может иметь каждая страница.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Включите шаг, а затем используйте его, чтобы установить количество строк на странице в этом разделе.
// Достаточно большой размер шрифта переместит некоторые строки вниз на следующую страницу, чтобы избежать перекрытия символов.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Смотрите также

* enum [SectionLayoutMode](../../sectionlayoutmode/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
