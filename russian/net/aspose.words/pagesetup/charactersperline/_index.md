---
title: PageSetup.CharactersPerLine
linktitle: CharactersPerLine
articleTitle: CharactersPerLine
second_title: Aspose.Words для .NET
description: Управляйте макетом документа с помощью свойства PageSetup CharactersPerLine. Легко настраивайте количество символов в строке для оптимальной читаемости и дизайна.
type: docs
weight: 100
url: /ru/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

Возвращает или задает количество символов в строке в сетке документа.

```csharp
public int CharactersPerLine { get; set; }
```

## Примечания

Минимальное значение свойства — 1. Максимальное значение зависит от ширины страницы и размера шрифта стиля Normal . Минимальный шаг символа — 90 процентов размера шрифта. Например, максимальное количество символов на строку страницы Letter с полями в один дюйм — 43.

По умолчанию свойство имеет значение, при котором шаг символа равен размеру шрифта стиля Normal .

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

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
