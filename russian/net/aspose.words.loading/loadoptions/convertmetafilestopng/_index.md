---
title: LoadOptions.ConvertMetafilesToPng
linktitle: ConvertMetafilesToPng
articleTitle: ConvertMetafilesToPng
second_title: Aspose.Words для .NET
description: Легко конвертируйте метафайлы WMF и EMF в формат PNG с помощью LoadOptions. Упростите управление изображениями и улучшите совместимость уже сегодня!
type: docs
weight: 30
url: /ru/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Возвращает или задает, следует ли преобразовывать метафайл (Wmf илиEmf ) изображения вPngформат изображения.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

## Примечания

Метафайлы (Wmf илиEmf ) — это несжатый формат изображения, который иногда требует слишком много оперативной памяти для хранения и обработки документа. Эта опция позволяет преобразовать все изображения метафайлов вPng при загрузке документа. Обратите внимание - преобразование векторной графики в растровую снижает качество изображений.

## Примеры

Показывает, как преобразовать WMF/EMF в PNG во время загрузки документа.

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

TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
