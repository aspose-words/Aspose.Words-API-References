---
title: PageSetup.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup Orientation, чтобы легко настроить макет страницы вашего документа. Оптимизируйте печать с помощью настраиваемых параметров ориентации!
type: docs
weight: 290
url: /ru/net/aspose.words/pagesetup/orientation/
---
## PageSetup.Orientation property

Возвращает или задает ориентацию страницы.

```csharp
public Orientation Orientation { get; set; }
```

## Примечания

Изменение`Orientation` свопы[`PageWidth`](../pagewidth/) и[`PageHeight`](../pageheight/).

## Примеры

Показывает, как настроить размер бумаги, ориентацию, поля, а также другие параметры раздела.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

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

* enum [Orientation](../../orientation/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
