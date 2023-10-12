---
title: RtfSaveOptions.SaveFormat
second_title: Справочник по API Aspose.Words для .NET
description: RtfSaveOptions свойство. Указывает формат в котором документ будет сохранен если используется этот объект параметров сохранения. Может быть толькоRtf .
type: docs
weight: 40
url: /ru/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

Указывает формат, в котором документ будет сохранен, если используется этот объект параметров сохранения. Может быть толькоRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Примеры

Показывает, как сохранить документ в формате .rtf с настраиваемыми параметрами.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Создайте объект «RtfSaveOptions», чтобы передать его методу «Save» документа, чтобы изменить способ его сохранения в RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Установите для свойства «ExportCompactSize» значение «true», чтобы
// уменьшаем размер сохраненного документа за счет совместимости текста справа налево.
options.ExportCompactSize = true;

// Установите для свойства «ExportImagesFotOldReaders» значение «true», чтобы использовать дополнительные ключевые слова, гарантирующие, что наш документ
// совместимо с программами чтения до Microsoft Word 97 и WordPad.
// Установите для свойства «ExportImagesFotOldReaders» значение «false», чтобы уменьшить размер документа,
// но не позволяем старым программам чтения читать любые неметафайлы или изображения BMP, которые может содержать документ.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../rtfsaveoptions/)
* сборка [Aspose.Words](../../../)


