---
title: NodeRendererBase.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words для .NET
description: Откройте для себя метод сохранения NodeRendererBase. Легко визуализируйте фигуры как изображения и сохраняйте их в файлы для бесшовной интеграции и повышения производительности.
type: docs
weight: 90
url: /ru/net/aspose.words.rendering/noderendererbase/save/
---
## Save(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save_2}

Преобразует форму в изображение и сохраняет в файл.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла изображения. Если файл с указанным именем уже существует, существующий файл перезаписывается. |
| saveOptions | ImageSaveOptions | Задает параметры, которые управляют тем, как форма отображается и сохраняется. Может быть`нулевой`. |

## Примеры

Показывает, как преобразовать объект Office Math в файл изображения в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Создаем объект "ImageSaveOptions" для передачи в метод "Save" рендерера узла для изменения
// как он преобразует узел OfficeMath в изображение.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Установите свойство «Масштаб» на 5, чтобы отрисовать объект в пять раз больше его исходного размера.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)

---

## Save(*string, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_3}

Визуализирует фигуру в изображение SVG и сохраняет в файл.

```csharp
public void Save(string fileName, SvgSaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла изображения. Если файл с указанным именем уже существует, существующий файл перезаписывается. |
| saveOptions | SvgSaveOptions | Задает параметры, которые управляют тем, как форма отображается и сохраняется. Может быть`нулевой`. |

## Примеры

Показывает, как передавать параметры сохранения при рендеринге офисной математики.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### Смотрите также

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)

---

## Save(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save}

Визуализирует форму в изображение и сохраняет в поток.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, в котором сохраняется изображение фигуры. |
| saveOptions | ImageSaveOptions | Задает параметры, которые управляют тем, как форма отображается и сохраняется. Может быть`нулевой` . Если это`нулевой`изображение будет сохранено в формате PNG. |

## Примеры

Показывает, как использовать средство визуализации фигур для экспорта фигур в файлы в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// В документе 7 фигур, включая одну групповую фигуру с 2 дочерними фигурами.
// Мы отобразим каждую фигуру в файле изображения в локальной файловой системе
// игнорируя при этом групповые фигуры, поскольку они не имеют внешнего вида.
// Это создаст 6 файлов изображений.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)

---

## Save(*Stream, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_1}

Отображает форму в виде изображения SVG и сохраняет в потоке.

```csharp
public void Save(Stream stream, SvgSaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, в котором сохраняется SVG-изображение фигуры. |
| saveOptions | SvgSaveOptions | Задает параметры, которые управляют тем, как форма отображается и сохраняется. Может быть`нулевой` . Если это`нулевой`, изображение будет сохранено с параметрами по умолчанию. |

## Примеры

Показывает, как передавать параметры сохранения при рендеринге офисной математики.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### Смотрите также

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)
