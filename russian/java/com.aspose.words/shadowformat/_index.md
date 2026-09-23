---
title: "ShadowFormat"
linktitle: "ShadowFormat"
second_title: "Aspose.Words для Java"
description: "Представляет форматирование тени для объекта в Java."
type: docs
weight: 610
url: /ru/java/com.aspose.words/shadowformat/
---

**Inheritance:**
java.lang.Object
```
public class ShadowFormat
```

Представляет форматирование тени для объекта.

Чтобы узнать больше, посетите статью документации [ Working with Graphic Elements ][Working with Graphic Elements].

 **Examples:** 

Показывает, как получить цвет тени.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```


[Working with Graphic Elements]: https://docs.aspose.com/words/java/working-with-graphic-elements/
## Методы

| Метод | Описание |
| --- | --- |
| [clear()](#clear) | Очищает формат тени. |
| [getColor()](#getColor) | Возвращает объект java.awt.Color, представляющий цвет тени. |
| [getTransparency()](#getTransparency) | Возвращает степень прозрачности эффекта тени в виде значения от 0.0 (непрозрачный) до 1.0 (прозрачный). |
| [getType()](#getType) | Получает указанный [ShadowType](../../com.aspose.words/shadowtype/) для ShadowFormat. |
| [getVisible()](#getVisible) | Возвращает  true  если форматирование, применённое к этому экземпляру, видно. |
| [setColor(Color value)](#setColor-java.awt.Color) | Устанавливает объект java.awt.Color, представляющий цвет тени. |
| [setTransparency(double value)](#setTransparency-double) | Устанавливает степень прозрачности эффекта тени как значение от 0.0 (непрозрачный) до 1.0 (прозрачный). |
| [setType(int value)](#setType-int) | Устанавливает указанный [ShadowType](../../com.aspose.words/shadowtype/) для ShadowFormat. |
### clear() {#clear}
```
public void clear()
```


Очищает формат тени.

 **Examples:** 

Показывает, как работать с форматированием тени для формы.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

### getColor() {#getColor}
```
public Color getColor()
```


Получает объект java.awt.Color, представляющий цвет тени. Значение по умолчанию — java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Показывает, как получить цвет тени.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

Показывает, как установить цвет с прозрачностью.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Returns:**
java.awt.Color - объект java.awt.Color, представляющий цвет тени.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Получает степень прозрачности эффекта тени как значение от 0.0 (непрозрачный) до 1.0 (прозрачный). Значение по умолчанию — 0.0.

 **Examples:** 

Показывает, как установить цвет с прозрачностью.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Returns:**
double - степень прозрачности эффекта тени как значение от 0.0 (непрозрачный) до 1.0 (прозрачный).
### getType() {#getType}
```
public int getType()
```


Получает указанный [ShadowType](../../com.aspose.words/shadowtype/) для ShadowFormat.

 **Remarks:** 

Установка нового типа тени сбросит значения Color и Transparency к значениям по умолчанию. Поэтому имеет смысл сначала задать желаемый тип тени, а затем уже значения Color и Transparency.

 **Examples:** 

Показывает, как получить цвет тени.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Returns:**
int - указанный [ShadowType](../../com.aspose.words/shadowtype/) для ShadowFormat. Возвращаемое значение является одной из констант [ShadowType](../../com.aspose.words/shadowtype/).
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Возвращает  true  если форматирование, применённое к этому экземпляру, видно.

 **Remarks:** 

В отличие от [clear()](../../com.aspose.words/shadowformat/\#clear), присвоение  false  свойству Visible не очищает форматирование, а лишь скрывает эффект формы.

 **Examples:** 

Показывает, как работать с форматированием тени для формы.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

**Returns:**
boolean -  true  если форматирование, применённое к этому экземпляру, видно.
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Устанавливает объект java.awt.Color, представляющий цвет тени. Значение по умолчанию — java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Показывает, как получить цвет тени.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

Показывает, как установить цвет с прозрачностью.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Объект java.awt.Color, представляющий цвет тени. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Устанавливает степень прозрачности эффекта тени как значение от 0.0 (непрозрачный) до 1.0 (прозрачный). Значение по умолчанию — 0.0.

 **Examples:** 

Показывает, как установить цвет с прозрачностью.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Степень прозрачности эффекта тени как значение от 0.0 (непрозрачный) до 1.0 (прозрачный). |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Устанавливает указанный [ShadowType](../../com.aspose.words/shadowtype/) для ShadowFormat.

 **Remarks:** 

Установка нового типа тени сбросит значения Color и Transparency к значениям по умолчанию. Поэтому имеет смысл сначала задать желаемый тип тени, а затем уже значения Color и Transparency.

 **Examples:** 

Показывает, как получить цвет тени.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Указанный [ShadowType](../../com.aspose.words/shadowtype/) для ShadowFormat. Значение должно быть одной из констант [ShadowType](../../com.aspose.words/shadowtype/). |

