---
title: FieldIf
second_title: Aspose.Words for Java API Reference
description: Implements the IF field.
type: docs
weight: 200
url: /java/com.aspose.words/fieldif/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldIf extends Field
```

Implements the IF field.

To learn more, visit the **Working with Fields** documentation article.

Compares the values designated by the expressions [getLeftExpression()](../../com.aspose.words/fieldif\#getLeftExpression--) / [setLeftExpression(java.lang.String)](../../com.aspose.words/fieldif\#setLeftExpression-java.lang.String-) and [getRightExpression()](../../com.aspose.words/fieldif\#getRightExpression--) / [setRightExpression(java.lang.String)](../../com.aspose.words/fieldif\#setRightExpression-java.lang.String-) in comparison using the operator designated by [getComparisonOperator()](../../com.aspose.words/fieldif\#getComparisonOperator--) / [setComparisonOperator(java.lang.String)](../../com.aspose.words/fieldif\#setComparisonOperator-java.lang.String-).

A field in the following format will be used as a mail merge source: \{ IF 0 = 0 "\{PatientsNameFML\}" "" \\\* MERGEFORMAT \}
## Methods

| Method | Description |
| --- | --- |
| [getMergeFieldName()](#getMergeFieldName--) |  |
| [canWorkAsMergeField()](#canWorkAsMergeField--) |  |
| [isMergeValueRequired()](#isMergeValueRequired--) |  |
| [getLeftExpression()](#getLeftExpression--) | Gets the left part of the comparison expression. |
| [setLeftExpression(String value)](#setLeftExpression-java.lang.String-) | Sets the left part of the comparison expression. |
| [getComparisonOperator()](#getComparisonOperator--) | Gets the comparison operator. |
| [setComparisonOperator(String value)](#setComparisonOperator-java.lang.String-) | Sets the comparison operator. |
| [getRightExpression()](#getRightExpression--) | Gets the right part of the comparison expression. |
| [setRightExpression(String value)](#setRightExpression-java.lang.String-) | Sets the right part of the comparison expression. |
| [getTrueText()](#getTrueText--) | Gets the text displayed if the comparison expression is true. |
| [setTrueText(String value)](#setTrueText-java.lang.String-) | Sets the text displayed if the comparison expression is true. |
| [getFalseText()](#getFalseText--) | Gets the text displayed if the comparison expression is false. |
| [setFalseText(String value)](#setFalseText-java.lang.String-) | Sets the text displayed if the comparison expression is false. |
| [evaluateCondition()](#evaluateCondition--) | Evaluates the condition. |
### getMergeFieldName() {#getMergeFieldName--}
```
public String getMergeFieldName()
```




**Returns:**
java.lang.String
### canWorkAsMergeField() {#canWorkAsMergeField--}
```
public boolean canWorkAsMergeField()
```




**Returns:**
boolean
### isMergeValueRequired() {#isMergeValueRequired--}
```
public boolean isMergeValueRequired()
```




**Returns:**
boolean
### getLeftExpression() {#getLeftExpression--}
```
public String getLeftExpression()
```


Gets the left part of the comparison expression.

**Returns:**
java.lang.String - The left part of the comparison expression.
### setLeftExpression(String value) {#setLeftExpression-java.lang.String-}
```
public void setLeftExpression(String value)
```


Sets the left part of the comparison expression.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The left part of the comparison expression. |

### getComparisonOperator() {#getComparisonOperator--}
```
public String getComparisonOperator()
```


Gets the comparison operator.

**Returns:**
java.lang.String - The comparison operator.
### setComparisonOperator(String value) {#setComparisonOperator-java.lang.String-}
```
public void setComparisonOperator(String value)
```


Sets the comparison operator.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The comparison operator. |

### getRightExpression() {#getRightExpression--}
```
public String getRightExpression()
```


Gets the right part of the comparison expression.

**Returns:**
java.lang.String - The right part of the comparison expression.
### setRightExpression(String value) {#setRightExpression-java.lang.String-}
```
public void setRightExpression(String value)
```


Sets the right part of the comparison expression.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The right part of the comparison expression. |

### getTrueText() {#getTrueText--}
```
public String getTrueText()
```


Gets the text displayed if the comparison expression is true.

**Returns:**
java.lang.String - The text displayed if the comparison expression is true.
### setTrueText(String value) {#setTrueText-java.lang.String-}
```
public void setTrueText(String value)
```


Sets the text displayed if the comparison expression is true.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text displayed if the comparison expression is true. |

### getFalseText() {#getFalseText--}
```
public String getFalseText()
```


Gets the text displayed if the comparison expression is false.

**Returns:**
java.lang.String - The text displayed if the comparison expression is false.
### setFalseText(String value) {#setFalseText-java.lang.String-}
```
public void setFalseText(String value)
```


Sets the text displayed if the comparison expression is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text displayed if the comparison expression is false. |

### evaluateCondition() {#evaluateCondition--}
```
public int evaluateCondition()
```


Evaluates the condition.

**Returns:**
int - A [FieldIfComparisonResult](../../com.aspose.words/fieldifcomparisonresult) value that represents the result of the condition evaluation. The returned value is one of [FieldIfComparisonResult](../../com.aspose.words/fieldifcomparisonresult) constants.
