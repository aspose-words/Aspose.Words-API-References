---
title: FixedPageSaveOptions.NumeralFormat
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words для .NET
description: FixedPageSaveOptions NumeralFormat свойство. Получает или устанавливаетNumeralFormat используется для отрисовки цифр. По умолчанию используются европейские цифры на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

Получает или устанавливает[`NumeralFormat`](../../numeralformat/) используется для отрисовки цифр. По умолчанию используются европейские цифры.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

## Примечания

Если значение этого свойства изменено и макет страницы уже создан, то [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) вызывается автоматически для обновления любых изменений.

## Примеры

Показывает, как установить числовой формат, используемый при сохранении в PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства «NumeralFormat» значение «NumeralFormat.ArabicIndic», чтобы
// использовать глифы из диапазона от U+0660 до U+0669 в качестве чисел.
// Установите для свойства "NumeralFormat" значение "NumeralFormat.Context", чтобы
// ищем локаль, чтобы определить, какое количество глифов использовать.
// Установите для свойства «NumeralFormat» значение «NumeralFormat.easternArabicIndic», чтобы
// использовать глифы из диапазона от U+06F0 до U+06F9 в качестве чисел.
// Установите для свойства «NumeralFormat» значение «NumeralFormat.European», чтобы использовать европейские цифры.
// Установите для свойства «NumeralFormat» значение «NumeralFormat.System», чтобы определить набор символов из региональных настроек.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Смотрите также

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
