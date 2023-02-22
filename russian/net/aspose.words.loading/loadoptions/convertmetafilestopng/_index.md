---
title: LoadOptions.ConvertMetafilesToPng
second_title: Справочник по API Aspose.Words для .NET
description: LoadOptions свойство. Получает или задает следует ли преобразовывать метафайл Wmf или жеEmf  изображения вPng формат изображения.
type: docs
weight: 30
url: /ru/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Получает или задает, следует ли преобразовывать метафайл (Wmf или жеEmf ) изображения вPng формат изображения.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

### Примечания

Метафайлы (Wmf или жеEmf ) представляет собой несжатый формат изображения и иногда требует много оперативной памяти для хранения и обработки документа. Этот параметр позволяет преобразовать все изображения метафайла вPng при загрузке документа. Обратите внимание - преобразование векторной графики в растр снижает качество изображений.

### Примеры

Показывает, как конвертировать WMF/EMF в PNG во время загрузки документа.

```csharp
Document doc = new Document();

            Shape shape = new Shape(doc, ShapeType.Image);
            shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
            shape.Width = 100;
            shape.Height = 100;

            doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

            doc.Save(ArtifactsDir + "Image.CreateImageDirectly.docx");

            shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

            TestUtil.VerifyImageInShape(1600, 1600, ImageType.Wmf, shape);

            LoadOptions loadOptions = new LoadOptions();
            loadOptions.ConvertMetafilesToPng = true;

            doc = new Document(ArtifactsDir + "Image.CreateImageDirectly.docx", loadOptions);
            shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

#if NET48
            TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
#elif NET5_0_OR_GREATER
            TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
#endif
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../loadoptions/)
* сборка [Aspose.Words](../../../)


