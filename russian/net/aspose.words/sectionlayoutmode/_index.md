---
title: Enum SectionLayoutMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.SectionLayoutMode перечисление. Указывает режим макета для раздела позволяющий определить поведение сетки документа.
type: docs
weight: 5460
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
| Default | `0` | Указывает, что сетка документа не должна применяться к содержимому соответствующего раздела в документе. |
| Grid | `1` | Указывает, что соответствующий раздел должен иметь как дополнительный шаг строки, так и шаг символа , добавленный к каждой строке и символу в нем, чтобы поддерживать определенное количество строк на странице и символов в строке. Символы не будут автоматически выравниваться с линиями сетки на печатаю. |
| LineGrid | `2` | Указывает, что в соответствующем разделе должен быть добавлен дополнительный шаг строки к каждой строке внутри it , чтобы сохранить указанное количество строк на странице. |
| SnapToChars | `3` | Указывает, что соответствующий раздел должен иметь как дополнительный шаг строки, так и шаг символа , добавленный к каждой строке и символу в ней, чтобы поддерживать определенное количество строк на странице и символов в строке. Символы будут автоматически выравниваться по линиям сетки при наборе текста. |

### Примеры

Показывает, как указать число символов, которое может содержаться в каждой строке.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Включите питчинг, а затем используйте его, чтобы установить количество символов в строке в этом разделе.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Количество символов также зависит от размера шрифта.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


