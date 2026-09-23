---
title: "HorizontalRuleFormat"
linktitle: "HorizontalRuleFormat"
second_title: "Aspose.Words для Java"
description: "Представляет форматирование горизонтальной линии в Java."
type: docs
weight: 376
url: /ru/java/com.aspose.words/horizontalruleformat/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleFormat
```

Представляет форматирование горизонтального правила.

Чтобы узнать больше, посетите статью документации [ Working with Shapes ][Working with Shapes].

 **Examples:** 

Показывает, как вставить форму горизонтального правила и настроить её форматирование.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Методы

| Метод | Описание |
| --- | --- |
| [getAlignment()](#getAlignment) | Получает выравнивание горизонтальной линии. |
| [getColor()](#getColor) | Получает цвет кисти, заполняющей горизонтальную линию. |
| [getHeight()](#getHeight) | Получает высоту горизонтальной линии. |
| [getNoShade()](#getNoShade) | Указывает наличие 3D‑теней для горизонтальной линии. |
| [getWidthPercent()](#getWidthPercent) | Получает длину указанной горизонтальной линии, выраженную в процентах от ширины окна. |
| [setAlignment(int value)](#setAlignment-int) | Устанавливает выравнивание горизонтальной линии. |
| [setColor(Color value)](#setColor-java.awt.Color) | Устанавливает цвет кисти, заполняющей горизонтальную линию. |
| [setHeight(double value)](#setHeight-double) | Устанавливает высоту горизонтальной линии. |
| [setNoShade(boolean value)](#setNoShade-boolean) | Указывает наличие 3D‑теней для горизонтальной линии. |
| [setWidthPercent(double value)](#setWidthPercent-double) | Устанавливает длину указанной горизонтальной линии, выраженную в процентах от ширины окна. |
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Получает выравнивание горизонтальной линии.

 **Remarks:** 

Значение по умолчанию: [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

Показывает, как вставить форму горизонтального правила и настроить её форматирование.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
int — Выравнивание горизонтальной линии. Возвращаемое значение является одной из констант [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/).
### getColor() {#getColor}
```
public Color getColor()
```


Получает цвет кисти, заполняющей горизонтальную линию.

 **Remarks:** 

Это сокращение к свойству [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color).

Значение по умолчанию: java.awt.Color\#getGray().getGray().

 **Examples:** 

Показывает, как вставить форму горизонтального правила и настроить её форматирование.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
java.awt.Color — Цвет кисти, заполняющей горизонтальную линию.
### getHeight() {#getHeight}
```
public double getHeight()
```


Получает высоту горизонтальной линии.

**Returns:**
double — Высота горизонтальной линии.
### getNoShade() {#getNoShade}
```
public boolean getNoShade()
```


Указывает наличие 3D‑теней для горизонтальной линии. Если  true , то горизонтальная линия без 3D‑теней и используется сплошной цвет.

 **Remarks:** 

Значение по умолчанию — false.

 **Examples:** 

Показывает, как вставить форму горизонтального правила и настроить её форматирование.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getWidthPercent() {#getWidthPercent}
```
public double getWidthPercent()
```


Получает длину указанной горизонтальной линии, выраженную в процентах от ширины окна.

**Returns:**
double — Длина указанной горизонтальной линии, выраженная в процентах от ширины окна.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Устанавливает выравнивание горизонтальной линии.

 **Remarks:** 

Значение по умолчанию: [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

Показывает, как вставить форму горизонтального правила и настроить её форматирование.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Выравнивание горизонтальной линии. Значение должно быть одним из констант [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/). |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Устанавливает цвет кисти, заполняющей горизонтальную линию.

 **Remarks:** 

Это сокращение к свойству [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color).

Значение по умолчанию: java.awt.Color\#getGray().getGray().

 **Examples:** 

Показывает, как вставить форму горизонтального правила и настроить её форматирование.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Цвет кисти, заполняющий горизонтальную линию. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Устанавливает высоту горизонтальной линии.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Высота горизонтальной линии. |

### setNoShade(boolean value) {#setNoShade-boolean}
```
public void setNoShade(boolean value)
```


Указывает наличие 3D‑теней для горизонтальной линии. Если  true , то горизонтальная линия без 3D‑теней и используется сплошной цвет.

 **Remarks:** 

Значение по умолчанию — false.

 **Examples:** 

Показывает, как вставить форму горизонтального правила и настроить её форматирование.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setWidthPercent(double value) {#setWidthPercent-double}
```
public void setWidthPercent(double value)
```


Устанавливает длину указанной горизонтальной линии, выраженную в процентах от ширины окна.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | double | Длина указанной горизонтальной линии, выраженная в процентах от ширины окна. |

