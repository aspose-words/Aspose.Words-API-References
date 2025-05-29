---
title: XlsxSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words для .NET
description: Откройте для себя свойство XlsxSaveOptions CompressionLevel, чтобы оптимизировать сохранение документов с помощью настраиваемых параметров сжатия для эффективного управления файлами.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/xlsxsaveoptions/compressionlevel/
---
## XlsxSaveOptions.CompressionLevel property

Указывает уровень сжатия, используемый для сохранения документа. Значение по умолчанию:Normal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
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

* enum [CompressionLevel](../../compressionlevel/)
* class [XlsxSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
