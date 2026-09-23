---
title: "FieldIfComparisonResult"
linktitle: "FieldIfComparisonResult"
second_title: "Aspose.Words для Java"
description: "Указывает результат оценки условия поля IF в Java."
type: docs
weight: 244
url: /ru/java/com.aspose.words/fieldifcomparisonresult/
---

**Inheritance:**
java.lang.Object
```
public class FieldIfComparisonResult
```

Указывает результат оценки условия поля IF.

 **Examples:** 

Показывает, как вставить поле IF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Statement 1: ");
 FieldIf field = (FieldIf) builder.insertField(FieldType.FIELD_IF, true);
 field.setLeftExpression("0");
 field.setComparisonOperator("=");
 field.setRightExpression("1");

 // The IF field will display a string from either its "TrueText" property,
 // or its "FalseText" property, depending on the truth of the statement that we have constructed.
 field.setTrueText("True");
 field.setFalseText("False");
 field.update();

 // In this case, "0 = 1" is incorrect, so the displayed result will be "False".
 Assert.assertEquals(" IF  0 = 1 True False", field.getFieldCode());
 Assert.assertEquals(FieldIfComparisonResult.FALSE, field.evaluateCondition());
 Assert.assertEquals("False", field.getResult());

 builder.write("\nStatement 2: ");
 field = (FieldIf) builder.insertField(FieldType.FIELD_IF, true);
 field.setLeftExpression("5");
 field.setComparisonOperator("=");
 field.setRightExpression("2 + 3");
 field.setTrueText("True");
 field.setFalseText("False");
 field.update();

 // This time the statement is correct, so the displayed result will be "True".
 Assert.assertEquals(" IF  5 = \"2 + 3\" True False", field.getFieldCode());
 Assert.assertEquals(FieldIfComparisonResult.TRUE, field.evaluateCondition());
 Assert.assertEquals("True", field.getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.IF.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [ERROR](#ERROR) | В условии есть ошибка. |
| [FALSE](#FALSE) | Условие ложно. |
| [TRUE](#TRUE) | Условие истинно. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String fieldIfComparisonResultName)](#fromName-java.lang.String) |  |
| [getName(int fieldIfComparisonResult)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fieldIfComparisonResult)](#toString-int) |  |
### ERROR {#ERROR}
```
public static int ERROR
```


В условии есть ошибка.

### FALSE {#FALSE}
```
public static int FALSE
```


Условие ложно.

### TRUE {#TRUE}
```
public static int TRUE
```


Условие истинно.

### length {#length}
```
public static int length
```


### fromName(String fieldIfComparisonResultName) {#fromName-java.lang.String}
```
public static int fromName(String fieldIfComparisonResultName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldIfComparisonResultName | java.lang.String |  |

**Returns:**
int
### getName(int fieldIfComparisonResult) {#getName-int}
```
public static String getName(int fieldIfComparisonResult)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldIfComparisonResult | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fieldIfComparisonResult) {#toString-int}
```
public static String toString(int fieldIfComparisonResult)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldIfComparisonResult | int |  |

**Returns:**
java.lang.String
