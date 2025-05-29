---
title: XlsxSaveOptions.SectionMode
linktitle: SectionMode
articleTitle: SectionMode
second_title: Aspose.Words для .NET
description: Узнайте, как свойство XlsxSaveOptions SectionMode оптимизирует обработку разделов для экспорта XLSX, обеспечивая бесперебойное управление документами и несколькими рабочими листами.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/xlsxsaveoptions/sectionmode/
---
## XlsxSaveOptions.SectionMode property

Возвращает или задает способ обработки разделов при сохранении в выходной документ XLSX. Значение по умолчанию:MultipleWorksheets .

```csharp
public XlsxSectionMode SectionMode { get; set; }
```

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

* enum [XlsxSectionMode](../../xlsxsectionmode/)
* class [XlsxSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
