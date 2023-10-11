---
title: RtfSaveOptions.ExportCompactSize
second_title: Справочник по API Aspose.Words для .NET
description: RtfSaveOptions свойство. Позволяет уменьшать размер выходных документов RTF но если они содержат текст RTL справа налево он будет отображаться неправильно. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 20
url: /ru/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Позволяет уменьшать размер выходных документов RTF, но если они содержат текст RTL (справа налево), он будет отображаться неправильно. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportCompactSize { get; set; }
```

### Примечания

Если документ, который вы хотите преобразовать в RTF с помощью Aspose.Words, не содержит текста, написанного справа налево на таких языках, как арабский, вы можете установить для этой опции значение`истинный` , чтобы уменьшить размер результирующего RTF.

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

* class [RtfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../rtfsaveoptions/)
* сборка [Aspose.Words](../../../)


