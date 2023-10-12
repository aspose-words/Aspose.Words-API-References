---
title: LoadOptions.ConvertMetafilesToPng
second_title: Справочник по API Aspose.Words для .NET
description: LoadOptions свойство. Получает или задает необходимость преобразования метафайла Wmf илиEmf  изображения дляPng формат изображения.
type: docs
weight: 30
url: /ru/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Получает или задает необходимость преобразования метафайла (Wmf илиEmf ) изображения дляPng формат изображения.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

### Примечания

Метафайлы (Wmf илиEmf ) — это несжатый формат изображения, и иногда для хранения и обработки документа требуется много оперативной памяти. Эта опция позволяет конвертировать все изображения метафайлов вPng при загрузке документа. Обратите внимание: преобразование векторной графики в растровую снижает качество изображений.

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


