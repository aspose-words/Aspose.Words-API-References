---
title: PageSetup.LinesPerPage
second_title: Справочник по API Aspose.Words для .NET
description: PageSetup свойство. Получает или задает количество строк на странице в сетке документа.
type: docs
weight: 240
url: /ru/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Получает или задает количество строк на странице в сетке документа.

```csharp
public int LinesPerPage { get; set; }
```

### Примечания

Минимальное значение свойства равно 1. Максимальное значение зависит от высоты страницы и размера шрифта стиля Normal . Минимальный шаг строки составляет 136 процентов от размера шрифта. Например, максимальное количество строк на странице страницы Letter с полями в один дюйм равно 39.

По умолчанию свойство имеет значение, при котором шаг строки в 1,5 раза больше размера шрифта стиля Normal.

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

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../pagesetup/)
* сборка [Aspose.Words](../../../)


