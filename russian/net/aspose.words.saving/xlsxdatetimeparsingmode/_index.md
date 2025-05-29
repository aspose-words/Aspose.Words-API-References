---
title: XlsxDateTimeParsingMode Enum
linktitle: XlsxDateTimeParsingMode
articleTitle: XlsxDateTimeParsingMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление XlsxDateTimeParsingMode от Aspose.Words для эффективного анализа текста документа. Легко идентифицируйте значения даты и времени в ваших файлах!
type: docs
weight: 6510
url: /ru/net/aspose.words.saving/xlsxdatetimeparsingmode/
---
## XlsxDateTimeParsingMode enumeration

Указывает, как анализируется текст документа для определения значений даты и времени.

```csharp
public enum XlsxDateTimeParsingMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| UseCurrentLocale | `0` | Формат даты и времени, установленный для текущего потока, используется в первую очередь для разбора строковых значений. Если разбор не удается, пробуются другие распространенные форматы даты и времени. |
| Auto | `1` | Формат даты и времени, используемый в документе, определяется автоматически. Это может занять дополнительное время. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
