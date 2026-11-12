---
title: "Регулировка"
linktitle: "Регулировка"
second_title: "Aspose.Words для Java"
description: "Представляет значения регулировки, применяемые к указанной фигуре в Java."
type: docs
weight: 11
url: /ru/java/com.aspose.words/adjustment/
---

**Inheritance:**
java.lang.Object
```
public class Adjustment
```

Представляет значения корректировок, применяемые к указанной фигуре.

 **Examples:** 

Показывает, как работать с необработанными значениями корректировки.

```

 Document doc = new Document(getMyDir() + "Rounded rectangle shape.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 AdjustmentCollection adjustments = shape.getAdjustments();
 Assert.assertEquals(1, adjustments.getCount());

 Adjustment adjustment = adjustments.get(0);
 Assert.assertEquals("adj", adjustment.getName());
 Assert.assertEquals(16667, adjustment.getValue());

 adjustment.setValue(30000);

 doc.save(getArtifactsDir() + "Shape.Adjustments.docx");
 
```
## Методы

| Метод | Описание |
| --- | --- |
| [getName()](#getName) | Получает имя регулировки. |
| [getValue()](#getValue) | Получает сырое значение регулировки. |
| [setValue(int value)](#setValue-int) | Устанавливает сырое значение регулировки. |
### getName() {#getName}
```
public String getName()
```


Получает имя регулировки.

 **Examples:** 

Показывает, как работать с необработанными значениями корректировки.

```

 Document doc = new Document(getMyDir() + "Rounded rectangle shape.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 AdjustmentCollection adjustments = shape.getAdjustments();
 Assert.assertEquals(1, adjustments.getCount());

 Adjustment adjustment = adjustments.get(0);
 Assert.assertEquals("adj", adjustment.getName());
 Assert.assertEquals(16667, adjustment.getValue());

 adjustment.setValue(30000);

 doc.save(getArtifactsDir() + "Shape.Adjustments.docx");
 
```

**Returns:**
java.lang.String - Имя регулировки.
### getValue() {#getValue}
```
public int getValue()
```


Получает сырое значение регулировки.

 **Remarks:** 

Значение регулировки — это просто направляющая, в которой указана формула, основанная на значении. То есть для направляющей значения регулировки никаких вычислений не выполняется. Вместо этого эта направляющая задаёт параметр, который используется в вычислениях внутри направляющих фигур.

 **Examples:** 

Показывает, как работать с необработанными значениями корректировки.

```

 Document doc = new Document(getMyDir() + "Rounded rectangle shape.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 AdjustmentCollection adjustments = shape.getAdjustments();
 Assert.assertEquals(1, adjustments.getCount());

 Adjustment adjustment = adjustments.get(0);
 Assert.assertEquals("adj", adjustment.getName());
 Assert.assertEquals(16667, adjustment.getValue());

 adjustment.setValue(30000);

 doc.save(getArtifactsDir() + "Shape.Adjustments.docx");
 
```

**Returns:**
int - Необработанное значение регулировки.
### setValue(int value) {#setValue-int}
```
public void setValue(int value)
```


Устанавливает сырое значение регулировки.

 **Remarks:** 

Значение регулировки — это просто направляющая, в которой указана формула, основанная на значении. То есть для направляющей значения регулировки никаких вычислений не выполняется. Вместо этого эта направляющая задаёт параметр, который используется в вычислениях внутри направляющих фигур.

 **Examples:** 

Показывает, как работать с необработанными значениями корректировки.

```

 Document doc = new Document(getMyDir() + "Rounded rectangle shape.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 AdjustmentCollection adjustments = shape.getAdjustments();
 Assert.assertEquals(1, adjustments.getCount());

 Adjustment adjustment = adjustments.get(0);
 Assert.assertEquals("adj", adjustment.getName());
 Assert.assertEquals(16667, adjustment.getValue());

 adjustment.setValue(30000);

 doc.save(getArtifactsDir() + "Shape.Adjustments.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Необработанное значение регулировки. |

