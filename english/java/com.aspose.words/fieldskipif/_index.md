---
title: FieldSkipIf
second_title: Aspose.Words for Java API Reference
description: Implements the SKIPIF field.
type: docs
weight: 244
url: /java/com.aspose.words/fieldskipif/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldSkipIf extends Field
```

Implements the SKIPIF field.

To learn more, visit the **Working with Fields** documentation article.

Compares the values designated by the expressions [getLeftExpression()](../../com.aspose.words/fieldskipif\#getLeftExpression--) / [setLeftExpression(java.lang.String)](../../com.aspose.words/fieldskipif\#setLeftExpression-java.lang.String-) and [getRightExpression()](../../com.aspose.words/fieldskipif\#getRightExpression--) / [setRightExpression(java.lang.String)](../../com.aspose.words/fieldskipif\#setRightExpression-java.lang.String-) in comparison using the operator designated by [getComparisonOperator()](../../com.aspose.words/fieldskipif\#getComparisonOperator--) / [setComparisonOperator(java.lang.String)](../../com.aspose.words/fieldskipif\#setComparisonOperator-java.lang.String-). If the comparison is true, SKIPIF cancels the current merge document, moves to the next data record in the data source, and starts a new merge document. If the comparison is false, the current merge document is continued.
## Methods

| Method | Description |
| --- | --- |
| [getLeftExpression()](#getLeftExpression--) | Gets the left part of the comparison expression. |
| [setLeftExpression(String value)](#setLeftExpression-java.lang.String-) | Sets the left part of the comparison expression. |
| [getComparisonOperator()](#getComparisonOperator--) | Gets the comparison operator. |
| [setComparisonOperator(String value)](#setComparisonOperator-java.lang.String-) | Sets the comparison operator. |
| [getRightExpression()](#getRightExpression--) | Gets the right part of the comparison expression. |
| [setRightExpression(String value)](#setRightExpression-java.lang.String-) | Sets the right part of the comparison expression. |
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

