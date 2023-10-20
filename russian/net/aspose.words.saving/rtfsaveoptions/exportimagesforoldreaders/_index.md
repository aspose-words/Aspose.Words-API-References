---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: Aspose.Words для .NET
description: RtfSaveOptions ExportImagesForOldReaders свойство. Указывает записываются ли ключевые слова для старых читателей в RTF или нет. Это может существенно повлиять на размер документа RTF. Значение по умолчаниюистинный  на С#.
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

«Старые программы чтения» — это приложения, выпущенные до Microsoft Word 97, а также WordPad. Если этот параметр установлен`истинный` Aspose.Words записывает дополнительные ключевые слова RTF. Эти ключевые слова позволяют корректно отображать документ при открытии в приложении «старой программы чтения» , но могут значительно увеличить размер документа.

Если вы установите эту опцию на`ЛОЖЬ`, то в "старых читалках" будут отображаться только изображения в форматах WMF, EMF и BMP .

## Примеры

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

* class [RtfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
