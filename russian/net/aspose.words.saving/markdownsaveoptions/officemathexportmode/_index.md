---
title: MarkdownSaveOptions.OfficeMathExportMode
linktitle: OfficeMathExportMode
articleTitle: OfficeMathExportMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MarkdownSaveOptions OfficeMathExportMode для настройки вывода OfficeMath. Оптимизируйте свои файлы с помощью гибких настроек экспорта!
type: docs
weight: 120
url: /ru/net/aspose.words.saving/markdownsaveoptions/officemathexportmode/
---
## MarkdownSaveOptions.OfficeMathExportMode property

Указывает, как OfficeMath будет записан в выходной файл. Значение по умолчанию:Text .

```csharp
public MarkdownOfficeMathExportMode OfficeMathExportMode { get; set; }
```

## Примеры

Показывает, как OfficeMath будет записан в документ.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### Смотрите также

* enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* class [MarkdownSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
