---
title: PageVerticalAlignment Enum
linktitle: PageVerticalAlignment
articleTitle: PageVerticalAlignment
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.PageVerticalAlignment для оптимального выравнивания текста на страницах. Улучшите макет вашего документа с помощью точного вертикального выравнивания!
type: docs
weight: 5100
url: /ru/net/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enumeration

Задает вертикальное выравнивание текста на каждой странице.

```csharp
public enum PageVerticalAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Bottom | `3` | Текст выравнивается по нижнему краю страницы. |
| Center | `1` | Текст выравнивается по центру страницы. |
| Justify | `2` | Текст распространяется на всю страницу. |
| Top | `0` | Текст выравнивается по верхнему краю страницы. |

## Примеры

Показывает, как применять и отменять настройки страницы для разделов документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Измените свойства настройки страницы для текущего раздела конструктора и добавьте текст.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Если мы начнем новый раздел с помощью конструктора документов,
// он унаследует текущие свойства настройки страницы конструктора.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Мы можем вернуть свойства настройки страницы к значениям по умолчанию, используя метод «ClearFormatting».
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Смотрите также

* class [PageSetup](../pagesetup/)
* property [VerticalAlignment](../pagesetup/verticalalignment/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
