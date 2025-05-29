---
title: NumeralFormat Enum
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Saving.NumeralFormat для оптимального представления чисел в фиксированных форматах страниц. Улучшите рендеринг документов сегодня!
type: docs
weight: 6090
url: /ru/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

Указывает набор символов, который используется для представления чисел при отображении в фиксированных форматах страниц.

```csharp
public enum NumeralFormat
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| European | `0` | Европейские цифры: 0123456789. |
| ArabicIndic | `1` | Цифры, используемые в арабском языке: ٠١٢٣٤٥٦٧٨٩. Диапазон Unicode U+0660 - u+0669. |
| EasternArabicIndic | `2` | Цифры, используемые в персидском языке и языке урду: ۰۱۲۳۴۵۶۷۸۹. Диапазон Unicode U+06F0 - u+06F9. |
| Context | `3` | Набор символов определяется из контекста (локаль и свойство RTL). |
| System | `4` | ЭТА ОПЦИЯ НЕ ПОДДЕРЖИВАЕТСЯ. Набор символов определяется региональными настройками. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
