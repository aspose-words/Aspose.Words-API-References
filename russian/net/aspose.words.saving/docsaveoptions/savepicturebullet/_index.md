---
title: DocSaveOptions.SavePictureBullet
linktitle: SavePictureBullet
articleTitle: SavePictureBullet
second_title: Aspose.Words для .NET
description: Узнайте, как свойство DocSaveOptions SavePictureBullet улучшает вывод документа. Управляйте сохранением данных PictureBullet без усилий для достижения оптимальных результатов.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

Когда`ЛОЖЬ` , Данные PictureBullet не сохраняются в выходном документе. Значение по умолчанию:`истинный` .

```csharp
public bool SavePictureBullet { get; set; }
```

## Примечания

Эта опция предусмотрена для Word 97, который не может корректно работать с данными PictureBullet. Чтобы удалить данные PictureBullet, установите для параметра значение «false».

## Примеры

Показывает, как исключить данные PictureBullet из документа при сохранении.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
// Некоторые текстовые процессоры, такие как Microsoft Word 97, несовместимы с данными PictureBullet.
// Установив флаг в объекте SaveOptions,
// мы можем преобразовать все маркеры изображений в обычные маркеры при сохранении.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### Смотрите также

* class [DocSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
