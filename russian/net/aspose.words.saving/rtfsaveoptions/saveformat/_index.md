---
title: RtfSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство RtfSaveOptions SaveFormat, чтобы легко сохранять документы в формате RTF, обеспечивая совместимость и простой обмен.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть толькоRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Примеры

Показывает, как сохранить документ в формате .rtf с пользовательскими параметрами.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Создаем объект «RtfSaveOptions» для передачи методу «Save» документа, чтобы изменить способ сохранения в формате RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Установите свойство "ExportCompactSize" в значение "true" для
// уменьшить размер сохраненного документа за счет совместимости с текстом, написанным справа налево.
options.ExportCompactSize = true;

// Установите свойство "ExportImagesFotOldReaders" в значение "true", чтобы использовать дополнительные ключевые слова и гарантировать, что наш документ
// совместимо с программами чтения до Microsoft Word 97 и WordPad.
// Установите свойство "ExportImagesFotOldReaders" в значение "false", чтобы уменьшить размер документа,
// но не позволяйте старым читателям читать любые неметафайловые или BMP-изображения, которые может содержать документ.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
