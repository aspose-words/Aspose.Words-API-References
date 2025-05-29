---
title: PageSetup.OtherPagesTray
linktitle: OtherPagesTray
articleTitle: OtherPagesTray
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup OtherPagesTray, чтобы легко настроить параметры лотка для бумаги для вашего принтера. Оптимизируйте эффективность печати для каждого раздела!
type: docs
weight: 300
url: /ru/net/aspose.words/pagesetup/otherpagestray/
---
## PageSetup.OtherPagesTray property

Возвращает или задает лоток для бумаги (корзину), который будет использоваться для всех страниц раздела, кроме первой. Значение зависит от реализации (принтера).

```csharp
public int OtherPagesTray { get; set; }
```

## Примеры

Показывает, как заставить все разделы документа использовать лоток для бумаги по умолчанию выбранного принтера.

```csharp
Document doc = new Document();

// Найдите принтер по умолчанию, который мы будем использовать для печати этого документа.
// Вы можете определить конкретный принтер, используя свойство «PrinterName» объекта PrinterSettings.
PrinterSettings settings = new PrinterSettings();

// Значение лотка для бумаги, хранящееся в документах, зависит от принтера.
// Это означает, что приведенный ниже код сбрасывает все значения лотка для страниц, чтобы использовать лоток по умолчанию текущего принтера.
// Вы можете перечислить PrinterSettings.PaperSources, чтобы найти другие допустимые значения лотка для бумаги выбранного принтера.
foreach (Section section in doc.Sections.OfType<Section>())
{
    section.PageSetup.FirstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
    section.PageSetup.OtherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

Показывает, как настроить печать с использованием разных лотков принтера для разных форматов бумаги.

```csharp
Document doc = new Document();

// Найдите принтер по умолчанию, который мы будем использовать для печати этого документа.
// Вы можете определить конкретный принтер, используя свойство «PrinterName» объекта PrinterSettings.
PrinterSettings settings = new PrinterSettings();

// Это лоток, который мы будем использовать для страниц формата «А4».
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// Это лоток, который мы будем использовать для страниц формата «Letter».
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// Измените объект PageSettings этого раздела, чтобы Microsoft Word мог дать указание принтеру
// использовать один из лотков, указанных выше, в зависимости от размера бумаги в этом разделе.
foreach (Section section in doc.Sections.OfType<Section>())
{
    if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.Letter)
    {
        section.PageSetup.FirstPageTray = printerTrayForLetter;
        section.PageSetup.OtherPagesTray = printerTrayForLetter;
    }
    else if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.A4)
    {
        section.PageSetup.FirstPageTray = printerTrayForA4;
        section.PageSetup.OtherPagesTray = printerTrayForA4;
    }
}
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
