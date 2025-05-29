---
title: DocumentBuilder.PageSetup
linktitle: PageSetup
articleTitle: PageSetup
second_title: Aspose.Words для .NET
description: Изучите свойство PageSetup в DocumentBuilder, чтобы получить доступ к текущим настройкам страницы и раздела, что повысит эффективность форматирования и макета документа.
type: docs
weight: 160
url: /ru/net/aspose.words/documentbuilder/pagesetup/
---
## DocumentBuilder.PageSetup property

Возвращает объект, представляющий текущие настройки страницы и свойства раздела.

```csharp
public PageSetup PageSetup { get; }
```

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

* class [PageSetup](../../pagesetup/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
