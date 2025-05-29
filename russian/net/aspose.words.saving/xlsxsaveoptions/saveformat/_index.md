---
title: XlsxSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство XlsxSaveOptions SaveFormat, позволяющее легко сохранять документы в формате Xlsx, гарантируя совместимость и качество ваших файлов.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/xlsxsaveoptions/saveformat/
---
## XlsxSaveOptions.SaveFormat property

Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть толькоXlsx .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Примеры

Показывает, как сжать документ XLSX.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.CompressionLevel = CompressionLevel.Maximum;
xlsxSaveOptions.SaveFormat = SaveFormat.Xlsx;

doc.Save(ArtifactsDir + "XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XlsxSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
