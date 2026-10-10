---
title: "GlowFormat"
linktitle: "GlowFormat"
second_title: "Aspose.Words для Java"
description: "Представляет формат свечения для объекта в Java."
type: docs
weight: 358
url: /ru/java/com.aspose.words/glowformat/
---

**Inheritance:**
java.lang.Object
```
public class GlowFormat
```

Представляет свечение объекта.

 **Remarks:** 

Используйте свойство [ShapeBase.getGlow()](../../com.aspose.words/shapebase/\#getGlow) для доступа к свойствам свечения объекта. Вы не создаёте экземпляры класса [GlowFormat](../../com.aspose.words/glowformat/) напрямую.

 **Examples:** 

Показывает, как взаимодействовать с эффектом свечения формы.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```
## Методы

| Метод | Описание |
| --- | --- |
| [getColor()](#getColor) | Возвращает объект java.awt.Color, представляющий цвет для эффекта свечения. |
| [getRadius()](#getRadius) | Возвращает значение double, представляющее длину радиуса эффекта свечения в пунктах (pt). |
| [getTransparency()](#getTransparency) | Возвращает степень прозрачности эффекта свечения в виде значения от 0.0 (непрозрачный) до 1.0 (прозрачный). |
| [remove()](#remove) | Удаляет [GlowFormat](../../com.aspose.words/glowformat/) из родительского объекта. |
| [setColor(Color value)](#setColor-java.awt.Color) | Устанавливает объект java.awt.Color, представляющий цвет для эффекта свечения. |
| [setRadius(double value)](#setRadius-double) | Устанавливает значение double, представляющее длину радиуса эффекта свечения в пунктах (pt). |
| [setTransparency(double value)](#setTransparency-double) | Устанавливает степень прозрачности эффекта свечения в виде значения от 0.0 (непрозрачный) до 1.0 (прозрачный). |
### getColor() {#getColor}
```
public Color getColor()
```


Возвращает объект java.awt.Color, представляющий цвет для эффекта свечения. Значение по умолчанию — java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Показывает, как взаимодействовать с эффектом свечения формы.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Returns:**
java.awt.Color — объект java.awt.Color, представляющий цвет для эффекта свечения.
### getRadius() {#getRadius}
```
public double getRadius()
```


Возвращает значение double, представляющее длину радиуса эффекта свечения в пунктах (pt). Значение по умолчанию — 0.0.

 **Examples:** 

Показывает, как взаимодействовать с эффектом свечения формы.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Returns:**
double — значение double, представляющее длину радиуса эффекта свечения в пунктах (pt).
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Возвращает степень прозрачности эффекта свечения в виде значения от 0.0 (непрозрачный) до 1.0 (прозрачный). Значение по умолчанию — 0.0.

 **Examples:** 

Показывает, как взаимодействовать с эффектом свечения формы.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Returns:**
double — степень прозрачности эффекта свечения в виде значения от 0.0 (непрозрачный) до 1.0 (прозрачный).
### remove() {#remove}
```
public void remove()
```


Удаляет [GlowFormat](../../com.aspose.words/glowformat/) из родительского объекта.

 **Examples:** 

Показывает, как взаимодействовать с эффектом свечения формы.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Устанавливает объект java.awt.Color, представляющий цвет для эффекта свечения. Значение по умолчанию — java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Показывает, как взаимодействовать с эффектом свечения формы.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Объект java.awt.Color, представляющий цвет для эффекта свечения. |

### setRadius(double value) {#setRadius-double}
```
public void setRadius(double value)
```


Устанавливает значение double, представляющее длину радиуса эффекта свечения в пунктах (pt). Значение по умолчанию — 0.0.

 **Examples:** 

Показывает, как взаимодействовать с эффектом свечения формы.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Значение double, представляющее длину радиуса эффекта свечения в пунктах (pt). |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Устанавливает степень прозрачности эффекта свечения в виде значения от 0.0 (непрозрачный) до 1.0 (прозрачный). Значение по умолчанию — 0.0.

 **Examples:** 

Показывает, как взаимодействовать с эффектом свечения формы.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Степень прозрачности эффекта свечения в виде значения от 0.0 (непрозрачный) до 1.0 (прозрачный). |

