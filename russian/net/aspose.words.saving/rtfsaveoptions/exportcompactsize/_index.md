---
title: RtfSaveOptions.ExportCompactSize
linktitle: ExportCompactSize
articleTitle: ExportCompactSize
second_title: Aspose.Words для .NET
description: Оптимизируйте размер документа RTF с помощью свойства ExportCompactSize. Обеспечьте эффективное хранение, сохраняя целостность текста, даже с содержимым RTL.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Позволяет уменьшить размер выходных RTF-документов, но если они содержат текст RTL (справа налево), он будет отображаться неправильно. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportCompactSize { get; set; }
```

## Примечания

Если документ, который вы хотите преобразовать в RTF с помощью Aspose.Words, не содержит текста с письмом справа налево на таких языках, как арабский, то вы можете установить для этого параметра значение`истинный` для уменьшения размера результирующего RTF.

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

* class [RtfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
