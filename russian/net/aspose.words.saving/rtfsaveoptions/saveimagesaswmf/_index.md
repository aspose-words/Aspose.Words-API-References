---
title: RtfSaveOptions.SaveImagesAsWmf
second_title: Справочник по API Aspose.Words для .NET
description: RtfSaveOptions свойство. Когдаистинный все изображения будут сохранены как WMF.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/rtfsaveoptions/saveimagesaswmf/
---
## RtfSaveOptions.SaveImagesAsWmf property

Когда`истинный` все изображения будут сохранены как WMF.

```csharp
public bool SaveImagesAsWmf { get; set; }
```

### Примечания

Эта опция может помочь избежать предупреждающих сообщений WordPad.

### Примеры

Показывает, как преобразовать все изображения в документе в формат метафайла Windows при сохранении документа в формате RTF.

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

// Создайте объект «RtfSaveOptions», чтобы передать его методу «Save» документа, чтобы изменить способ его сохранения в RTF.
RtfSaveOptions rtfSaveOptions = new RtfSaveOptions();

// Установите для свойства «SaveImagesAsWmf» значение «true», чтобы преобразовать все изображения в документе в WMF при сохранении его в RTF.
// Это поможет таким читателям, как WordPad, прочитать наш документ.
// Установите для свойства SaveImagesAsWmf значение «false», чтобы сохранить исходный формат всех изображений в документе.
// когда мы сохраняем его в RTF. Это позволит сохранить качество изображений за счет совместимости со старыми устройствами чтения RTF.
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
* пространство имен [Aspose.Words.Saving](../../rtfsaveoptions/)
* сборка [Aspose.Words](../../../)


