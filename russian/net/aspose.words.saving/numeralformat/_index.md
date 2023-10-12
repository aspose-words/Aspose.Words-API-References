---
title: Enum NumeralFormat
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.NumeralFormat перечисление. Указывает набор символов который используется для представления чисел при рендеринге в фиксированные форматы страниц.
type: docs
weight: 5310
url: /ru/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

Указывает набор символов, который используется для представления чисел при рендеринге в фиксированные форматы страниц.

```csharp
public enum NumeralFormat
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| European | `0` | Европейские цифры: 0123456789. |
| ArabicIndic | `1` | Цифры, используемые в арабском языке: ٠١٢٣٤٥٦٧٨٩. Диапазон Юникода U+0660 – u+0669. |
| EasternArabicIndic | `2` | Цифры, используемые в персидском и урду: ۰۱۲۳۴۵۶۷۸۹. Диапазон Юникода U+06F0 - u+06F9. |
| Context | `3` | Набор символов определяется из контекста (локаль и свойство RTL). |
| System | `4` | ЭТА ОПЦИЯ НЕ ПОДДЕРЖИВАЕТСЯ. Набор символов определяется региональными настройками. |

### Примеры

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


