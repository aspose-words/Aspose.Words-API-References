---
title: Enum PageVerticalAlignment
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.PageVerticalAlignment перечисление. Задает вертикальное выравнивание текста на каждой странице.
type: docs
weight: 4130
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
| Bottom | `3` | Текст выровнен по нижнему краю страницы. |
| Center | `1` | Текст выровнен по середине страницы. |
| Justify | `2` | Текст распространяется на всю страницу. |
| Top | `0` | Текст выровнен по верхнему краю страницы. |

### Примеры

Показывает, как применять и возвращать параметры настройки страницы к разделам документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Измените свойства настройки страницы для текущего раздела конструктора и добавьте текст.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Если мы начинаем новый раздел с помощью конструктора документов,
// он унаследует текущие свойства настройки страницы компоновщика.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Мы можем вернуть его свойства настройки страницы к их значениям по умолчанию, используя метод «ClearFormatting».
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


