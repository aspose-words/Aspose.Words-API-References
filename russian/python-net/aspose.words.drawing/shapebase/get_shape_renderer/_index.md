---
title: ShapeBase.get_shape_renderer method
linktitle: get_shape_renderer method
articleTitle: get_shape_renderer method
second_title: Aspose.Words for Python
description: "ShapeBase.get_shape_renderer method. Creates and returns an object that can be used to render this shape into an image."
type: docs
weight: 670
url: /ru/python-net/aspose.words.drawing/shapebase/get_shape_renderer/
---

## get_shape_renderer() {#default}

Creates and returns an object that can be used to render this shape into an image.


```python
def get_shape_renderer(self):
    ...
```

### Remarks

This method just invokes the [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/) constructor and passes
this object as a parameter.




### Returns

The renderer object for this shape.


### Examples

Shows how to use a shape renderer to export shapes to files in the local file system.

```python
doc = aw.Document(file_name=MY_DIR + 'Various shapes.docx')
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
self.assertEqual(7, len(shapes))
# В документе есть 7 фигур, включая одну групповую фигуру с 2 дочерними фигурами.
# Мы отрендерим каждую фигуру в файл изображения в локальной файловой системе
# игнорируя групповые фигуры, так как у них нет внешнего вида.
# Это создаст 6 файлов изображений.
for shape in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))):
    renderer = shape.get_shape_renderer()
    options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
    renderer.save(file_name=ARTIFACTS_DIR + f'Shape.RenderAllShapes.{shape.name}.png', save_options=options)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

