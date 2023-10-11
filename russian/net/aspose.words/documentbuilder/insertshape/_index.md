---
title: DocumentBuilder.InsertShape
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Вставляет встроенную фигуру указанного типа и размера.
type: docs
weight: 440
url: /ru/net/aspose.words/documentbuilder/insertshape/
---
## InsertShape(ShapeType, double, double) {#insertshape_1}

Вставляет встроенную фигуру указанного типа и размера.

```csharp
public Shape InsertShape(ShapeType shapeType, double width, double height)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeType | ShapeType | Тип фигуры для вставки в документ. |
| width | Double | Ширина фигуры в пунктах. |
| height | Double | Высота фигуры в пунктах. |

### Возвращаемое значение

Узел формы, который был вставлен.

### Примеры

Показывает, как вставлять фигуры DML в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два типа переноса, которые могут иметь фигуры.
// 1 - Плавающий:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Встроенное:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Если вам нужно создать «непримитивные» фигуры, такие как SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded или DiagonalCornersRounded,
// затем сохраните документ со «Строгим» или «Переходным» соответствием, что позволяет сохранить форму в формате DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)

---

## InsertShape(ShapeType, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertshape}

Вставляет свободно плавающую фигуру с указанным положением, размером и типом переноса текста.

```csharp
public Shape InsertShape(ShapeType shapeType, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeType | ShapeType | Тип фигуры для вставки в документ |
| horzPos | RelativeHorizontalPosition | Указывает, откуда измеряется горизонтальное расстояние до фигуры. |
| left | Double | Расстояние в пунктах от начала координат до левой стороны фигуры. |
| vertPos | RelativeVerticalPosition | Указывает, откуда измеряется вертикальное расстояние до фигуры. |
| top | Double | Расстояние в точках от начала координат до верхней стороны фигуры. |
| width | Double | Ширина фигуры в пунктах. |
| height | Double | Ширина фигуры в пунктах. |
| wrapType | WrapType | Указывает, как обтекать фигуру текстом. |

### Возвращаемое значение

Узел формы, который был вставлен.

### Примеры

Показывает, как вставлять фигуры DML в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два типа переноса, которые могут иметь фигуры.
// 1 - Плавающий:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100, 
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Встроенное:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Если вам нужно создать «непримитивные» фигуры, такие как SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded или DiagonalCornersRounded,
// затем сохраните документ со «Строгим» или «Переходным» соответствием, что позволяет сохранить форму в формате DML.
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
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


