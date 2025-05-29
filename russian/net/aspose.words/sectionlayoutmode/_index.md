---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.SectionLayoutMode для оптимизации макетов разделов и улучшения поведения сетки документа для улучшенного управления форматированием.
type: docs
weight: 6580
url: /ru/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

Задает режим макета для раздела, позволяющий определить поведение сетки документа.

```csharp
public enum SectionLayoutMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Default | `0` | Указывает, что сетка документа не будет применяться к содержимому соответствующего раздела в документе. |
| Grid | `1` | Указывает, что соответствующий раздел должен иметь как дополнительный интервал между строками, так и интервал между символами , добавленный к каждой строке и символу в нем, чтобы поддерживать определенное количество строк на странице и символов в строке. Символы не будут автоматически выравниваться по линиям сетки при вводе текста. |
| LineGrid | `2` | Указывает, что соответствующий раздел должен иметь дополнительный межстрочный интервал, добавленный к каждой строке внутри него , чтобы поддерживать указанное количество строк на странице. |
| SnapToChars | `3` | Указывает, что соответствующий раздел должен иметь как дополнительный интервал между строками, так и интервал между символами , добавленный к каждой строке и символу в нем, чтобы поддерживать определенное количество строк на странице и символов в строке. Символы будут автоматически выравниваться по линиям сетки при вводе. |

## Примеры

Показывает, как указать количество символов, которое может содержать каждая строка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Включите питч, а затем используйте его для установки количества символов в строке в этом разделе.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Количество символов также зависит от размера шрифта.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
