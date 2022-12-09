---
title: FieldArgumentBuilder
second_title: Aspose.Words for Java API Reference
description: Builds a complex field argument consisting of fields nodes and plain text.
type: docs
weight: 156
url: /java/com.aspose.words/fieldargumentbuilder/
---

**Inheritance:**
java.lang.Object
```
public class FieldArgumentBuilder
```

Builds a complex field argument consisting of fields, nodes, and plain text.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Constructors

| Constructor | Description |
| --- | --- |
| [FieldArgumentBuilder()](#FieldArgumentBuilder) | Initializes an instance of the [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder) class. |
## Methods

| Method | Description |
| --- | --- |
| [addField(FieldBuilder fieldBuilder)](#addField-com.aspose.words.FieldBuilder) | Adds a field represented by a [FieldBuilder](../../com.aspose.words/fieldbuilder) to the argument. |
| [addNode(Inline node)](#addNode-com.aspose.words.Inline) | Adds a node to the argument. |
| [addText(String text)](#addText-java.lang.String) | Adds a plain text to the argument. |
| [buildBlock(DocumentBuilder documentBuilder)](#buildBlock-com.aspose.words.DocumentBuilder) |  |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### FieldArgumentBuilder() {#FieldArgumentBuilder}
```
public FieldArgumentBuilder()
```


Initializes an instance of the [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder) class.

### addField(FieldBuilder fieldBuilder) {#addField-com.aspose.words.FieldBuilder}
```
public FieldArgumentBuilder addField(FieldBuilder fieldBuilder)
```


Adds a field represented by a [FieldBuilder](../../com.aspose.words/fieldbuilder) to the argument.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldBuilder | [FieldBuilder](../../com.aspose.words/fieldbuilder) |  |

**Returns:**
[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder)
### addNode(Inline node) {#addNode-com.aspose.words.Inline}
```
public FieldArgumentBuilder addNode(Inline node)
```


Adds a node to the argument. Only text level nodes are supported at the moment.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Inline](../../com.aspose.words/inline) |  |

**Returns:**
[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder)
### addText(String text) {#addText-java.lang.String}
```
public FieldArgumentBuilder addText(String text)
```


Adds a plain text to the argument.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String |  |

**Returns:**
[FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder)
### buildBlock(DocumentBuilder documentBuilder) {#buildBlock-com.aspose.words.DocumentBuilder}
```
public void buildBlock(DocumentBuilder documentBuilder)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentBuilder | [DocumentBuilder](../../com.aspose.words/documentbuilder) |  |

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

