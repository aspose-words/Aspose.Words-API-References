---
title: XlsxSectionMode Enum
linktitle: XlsxSectionMode
articleTitle: XlsxSectionMode
second_title: Aspose.Words для .NET
description: Узнайте, как перечисление Aspose.Words XlsxSectionMode оптимизирует сохранение документов в формате XLSX, улучшая рабочий процесс и управление документами.
type: docs
weight: 6530
url: /ru/net/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enumeration

Указывает, как обрабатываются разделы при сохранении документа в формате XLSX.

```csharp
public enum XlsxSectionMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| MultipleWorksheets | `0` | Указывает, что для каждого раздела документа создается отдельный рабочий лист. |
| SingleWorksheet | `1` | Указывает, что все разделы документа сохраняются на одном листе. |

## Примеры

Показывает, как сохранить документ в виде отдельного рабочего листа.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Каждый раздел документа будет создан как отдельный рабочий лист.
// Используйте «SingleWorksheet» для отображения всех документов на одном рабочем листе.
XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.SectionMode = XlsxSectionMode.MultipleWorksheets;

doc.Save(ArtifactsDir + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
