---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: Aspose.Words для .NET
description: Aspose.Words.SectionLayoutMode перечисление. Указывает режим макета для раздела позволяющий определить поведение сетки документа на С#.
type: docs
weight: 5750
url: /ru/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

Указывает режим макета для раздела, позволяющий определить поведение сетки документа.

```csharp
public enum SectionLayoutMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Default | `0` | Указывает, что сетка документа не должна применяться к содержимому соответствующего раздела документа. |
| Grid | `1` | Указывает, что в соответствующем разделе должен быть добавлен как дополнительный шаг строки, так и шаг символов к каждой строке и символу внутри нее, чтобы поддерживать определенное количество строк на странице и символов в строке. Символы не будут автоматически выравниваться по линиям сетки на набрав. |
| LineGrid | `2` | Указывает, что в соответствующем разделе к каждой строке внутри it должен быть добавлен дополнительный шаг строки, чтобы поддерживать указанное количество строк на странице. |
| SnapToChars | `3` | Указывает, что в соответствующем разделе должен быть добавлен как дополнительный шаг строки, так и шаг символов к каждой строке и символу внутри нее, чтобы поддерживать определенное количество строк на странице и символов в строке. Символы будут автоматически выравниваться по линиям сетки при вводе. |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
