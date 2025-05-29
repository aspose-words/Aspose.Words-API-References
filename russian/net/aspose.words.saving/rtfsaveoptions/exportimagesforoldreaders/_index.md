---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: Aspose.Words для .NET
description: Оптимизируйте свои документы RTF с помощью свойства ExportImagesForOldReaders. Контролируйте включение ключевых слов для устаревших ридеров, влияющих на размер файла и производительность.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

Указывает, записываются ли ключевые слова для «старых читателей» в RTF или нет. Это может существенно повлиять на размер документа RTF. Значение по умолчанию:`истинный` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

## Примечания

«Старые ридеры» — это приложения до Microsoft Word 97, а также WordPad. Когда эта опция включена`истинный` Aspose.Words записывает дополнительные ключевые слова RTF. Эти ключевые слова позволяют корректно отображать документ при открытии в «старом» приложении для чтения, но могут значительно увеличить размер документа.

Если вы установите этот параметр на`ЛОЖЬ`то в «старых ридерах» будут отображаться только изображения в форматах WMF, EMF и BMP .

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
