---
title: PageSetup.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words для .NET
description: PageSetup VerticalAlignment свойство. Возвращает или задает вертикальное выравнивание текста на каждой странице документа или раздела на С#.
type: docs
weight: 450
url: /ru/net/aspose.words/pagesetup/verticalalignment/
---
## PageSetup.VerticalAlignment property

Возвращает или задает вертикальное выравнивание текста на каждой странице документа или раздела.

```csharp
public PageVerticalAlignment VerticalAlignment { get; set; }
```

## Примеры

Показывает, как применить и вернуть параметры настройки страницы к разделам документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Измените свойства настройки страницы для текущего раздела конструктора и добавьте текст.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Если мы начнем новый раздел с помощью построителя документов,
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

* enum [PageVerticalAlignment](../../pageverticalalignment/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
