---
title: RtfSaveOptions.SaveImagesAsWmf
linktitle: SaveImagesAsWmf
articleTitle: SaveImagesAsWmf
second_title: Aspose.Words для .NET
description: Узнайте, как свойство RtfSaveOptions SaveImagesAsWmf улучшает ваш документ, сохраняя все изображения в формате WMF для превосходного качества и совместимости.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/rtfsaveoptions/saveimagesaswmf/
---
## RtfSaveOptions.SaveImagesAsWmf property

Когда`истинный` все изображения будут сохранены как WMF.

```csharp
public bool SaveImagesAsWmf { get; set; }
```

## Примечания

Эта опция может помочь избежать предупреждающих сообщений WordPad.

## Примеры

Показывает, как преобразовать все изображения в документе в формат метафайла Windows, сохраняя документ как RTF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg");

Assert.AreEqual(ImageType.Jpeg, imageShape.ImageData.ImageType);

builder.InsertParagraph();
builder.Writeln("Png image:");
imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ImageType.Png, imageShape.ImageData.ImageType);

// Создаем объект «RtfSaveOptions» для передачи методу «Save» документа, чтобы изменить способ сохранения в формате RTF.
RtfSaveOptions rtfSaveOptions = new RtfSaveOptions();

// Установите свойство «SaveImagesAsWmf» в значение «true», чтобы преобразовать все изображения в документе в WMF при сохранении его в RTF.
// Это поможет таким программам, как WordPad, читать наш документ.
// Установите свойство "SaveImagesAsWmf" в значение "false", чтобы сохранить исходный формат всех изображений в документе
// поскольку мы сохраняем его в формате RTF. Это сохранит качество изображений за счет совместимости со старыми ридерами RTF.
rtfSaveOptions.SaveImagesAsWmf = saveImagesAsWmf;

doc.Save(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = new Document(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf");

NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

if (saveImagesAsWmf)
{
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[1]).ImageData.ImageType);
}
else
{
    Assert.AreEqual(ImageType.Jpeg, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Png, ((Shape)shapes[1]).ImageData.ImageType);
}
```

### Смотрите также

* class [RtfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
