---
title: ShapeBase.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "ShapeBase.name property. Gets or sets the optional shape name."
type: docs
weight: 420
url: /ru/python-net/aspose.words.drawing/shapebase/name/
---

## ShapeBase.name property

Gets or sets the optional shape name.


```python
@property
def name(self) -> str:
    ...

@name.setter
def name(self, value: str):
    ...

```

### Remarks

Default is empty string.

Cannot be ``None``, but can be an empty string.




### Examples

Shows how to use a shape's alternative text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CUBE, width=150, height=150)
shape.name = 'MyCube'
shape.alternative_text = 'Alt text for MyCube.'
# Мы можем получить доступ к альтернативному тексту фигуры, щёлкнув её правой кнопкой мыши, а затем через "Format AutoShape" -> "Alt Text".
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AltText.docx')
# Сохраните документ в HTML, а затем удалите связанное изображение, принадлежащее нашей фигуре.
# Браузер, который читает наш HTML, отобразит alt‑текст вместо отсутствующего изображения.
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AltText.html')
os.unlink(ARTIFACTS_DIR + 'Shape.AltText.001.png')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

