---
title: DocumentBuilder.InsertShape
linktitle: InsertShape
articleTitle: InsertShape
second_title: Aspose.Words для .NET
description: Легко добавляйте пользовательские встроенные фигуры с помощью метода InsertShape в DocumentBuilder. Улучшайте свои документы с помощью индивидуальных визуальных эффектов для эффектных презентаций!
type: docs
weight: 460
url: /ru/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), double, double*) {#insertshape_1}

Вставляет встроенную фигуру указанного типа и размера.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeType | ShapeType | Тип фигуры для вставки в документ. |
| width | Double | Ширина фигуры в точках. |
| height | Double | Высота фигуры в пунктах. |

### Возвращаемое значение

Узел формы, который был вставлен.

## Примеры

Показывает, как вставлять фигуры DML в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два типа обтекания, которые могут быть у фигур.
// 1 - Плавающий:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Встроенный:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Если вам нужно создать «не примитивные» формы, такие как SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded или DiagonalCornersRounded,
// затем сохраните документ с соответствием «Строгий» или «Переходный», что позволяет сохранить форму как DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertShape(*[ShapeType](../../../aspose.words.drawing/shapetype/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertshape}

Вставляет свободно плавающую фигуру с указанным положением, размером и типом обтекания текстом.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeType | ShapeType | Тип фигуры для вставки в документ |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется горизонтальное расстояние до фигуры. |
| left | Double | Расстояние в точках от начала координат до левой стороны фигуры. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется вертикальное расстояние до фигуры. |
| top | Double | Расстояние в точках от начала координат до верхней стороны фигуры. |
| width | Double | Ширина фигуры в точках. |
| height | Double | Высота фигуры в пунктах. |
| wrapType | WrapType | Указывает, как обтекать фигуру текстом. |

### Возвращаемое значение

Узел формы, который был вставлен.

## Примеры

Показывает, как вставлять фигуры DML в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два типа обтекания, которые могут быть у фигур.
// 1 - Плавающий:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Встроенный:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Если вам нужно создать «не примитивные» формы, такие как SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded или DiagonalCornersRounded,
// затем сохраните документ с соответствием «Строгий» или «Переходный», что позволяет сохранить форму как DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
