---
title: ImageData.FitImageToShape
linktitle: FitImageToShape
articleTitle: FitImageToShape
second_title: Aspose.Words для .NET
description: Оптимизируйте изображения с помощью метода FitImageToShape, обеспечивающего идеальное выравнивание пропорций в рамках Shape для создания потрясающих визуальных презентаций.
type: docs
weight: 190
url: /ru/net/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData.FitImageToShape method

Подгоняет данные изображения под фрейм Shape таким образом, чтобы соотношение сторон данных изображения соответствовало соотношению сторон фрейма Shape.

```csharp
public void FitImageToShape()
```

## Примеры

Показывает, как подогнать данные изображения под рамку Shape.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте форму изображения и оставьте ее ориентацию в состоянии по умолчанию.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 300, 450);
shape.ImageData.SetImage(ImageDir + "Barcode.png");
shape.ImageData.FitImageToShape();

doc.Save(ArtifactsDir + "Shape.FitImageToShape.docx");
```

### Смотрите также

* class [ImageData](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
