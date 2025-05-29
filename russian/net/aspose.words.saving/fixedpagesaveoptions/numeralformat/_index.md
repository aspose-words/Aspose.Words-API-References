---
title: FixedPageSaveOptions.NumeralFormat
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FixedPageSaveOptions NumeralFormat для настройки отображения цифр. Легко переключайтесь на европейские цифры для улучшенного представления документа.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

Получает или устанавливает[`NumeralFormat`](../../numeralformat/) используется для отображения цифр. По умолчанию используются европейские цифры.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

## Примечания

Если значение этого свойства изменено и макет страницы уже построен, то [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) вызывается автоматически для обновления любых изменений.

## Примеры

Показывает, как задать числовой формат, используемый при сохранении в PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите свойство "NumeralFormat" на "NumeralFormat.ArabicIndic" для
// используйте глифы из диапазона U+0660 – U+0669 в качестве чисел.
// Установите свойство "NumeralFormat" в "NumeralFormat.Context" для
// найдите локаль, чтобы определить, какое количество глифов использовать.
// Установите свойство "NumeralFormat" на "NumeralFormat.EasternArabicIndic" для
// используйте глифы из диапазона U+06F0 – U+06F9 в качестве чисел.
// Установите свойство "NumeralFormat" на "NumeralFormat.European", чтобы использовать европейские цифры.
// Установите свойство "NumeralFormat" в значение "NumeralFormat.System", чтобы определить набор символов из региональных настроек.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Смотрите также

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
