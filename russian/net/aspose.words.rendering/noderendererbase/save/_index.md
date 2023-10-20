---
title: NodeRendererBase.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words для .NET
description: NodeRendererBase Save метод. Преобразует форму в изображение и сохраняет в файл на С#.
type: docs
weight: 90
url: /ru/net/aspose.words.rendering/noderendererbase/save/
---
## Save(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save_1}

Преобразует форму в изображение и сохраняет в файл.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла изображения. Если файл с указанным именем уже существует, существующий файл перезаписывается. |
| saveOptions | ImageSaveOptions | Указывает параметры, управляющие отрисовкой и сохранением фигуры. Возможно`нулевой`. |

## Примеры

Показывает, как преобразовать объект Office Math в файл изображения в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Создаем объект ImageSaveOptions для передачи методу Save средства рендеринга узла для изменения
// как он преобразует узел OfficeMath в изображение.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Установите для свойства Scale значение 5, чтобы отобразить объект в пять раз больше его исходного размера.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)

---

## Save(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save}

Преобразует фигуру в изображение и сохраняет в поток.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, в котором сохраняется изображение фигуры. |
| saveOptions | ImageSaveOptions | Указывает параметры, управляющие отрисовкой и сохранением фигуры. Возможно`нулевой` . Если это`нулевой`, изображение будет сохранено в формате PNG. |

## Примеры

Показывает, как использовать средство рендеринга фигур для экспорта фигур в файлы в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// В документе 7 фигур, включая одну групповую фигуру с двумя дочерними фигурами.
// Мы преобразуем каждую фигуру в файл изображения в локальной файловой системе
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
