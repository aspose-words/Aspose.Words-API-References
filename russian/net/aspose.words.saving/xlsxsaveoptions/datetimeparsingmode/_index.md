---
title: XlsxSaveOptions.DateTimeParsingMode
linktitle: DateTimeParsingMode
articleTitle: DateTimeParsingMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DateTimeParsingMode в XlsxSaveOptions, чтобы настроить способ анализа дат и времени в вашем документе, обеспечивая точную интерпретацию данных.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/xlsxsaveoptions/datetimeparsingmode/
---
## XlsxSaveOptions.DateTimeParsingMode property

Возвращает или задает режим, который определяет, как анализируется текст документа для определения значений даты и времени. Значение по умолчанию:UseCurrentLocale .

```csharp
public XlsxDateTimeParsingMode DateTimeParsingMode { get; set; }
```

## Примеры

Показывает, как настроить автоматическое определение формата даты и времени.

```csharp
Document doc = new Document(MyDir + "Xlsx DateTime.docx");

XlsxSaveOptions saveOptions = new XlsxSaveOptions();
// Укажите, используя автоматическое определение формата даты и времени.
saveOptions.DateTimeParsingMode = XlsxDateTimeParsingMode.Auto;

doc.Save(ArtifactsDir + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
```

### Смотрите также

* enum [XlsxDateTimeParsingMode](../../xlsxdatetimeparsingmode/)
* class [XlsxSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
