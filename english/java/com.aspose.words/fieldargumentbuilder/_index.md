---
title: FieldArgumentBuilder
second_title: Aspose.Words for Java API Reference
description: Builds a complex field argument consisting of fields nodes and plain text.
type: docs
weight: 155
url: /java/com.aspose.words/fieldargumentbuilder/
---

**Inheritance:**
java.lang.Object
```
public class FieldArgumentBuilder
```

Builds a complex field argument consisting of fields, nodes, and plain text.

To learn more, visit the **Working with Fields** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [FieldArgumentBuilder()](#FieldArgumentBuilder--) | Initializes an instance of the [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder) class. |
## Methods

| Method | Description |
| --- | --- |
| [addText(String text)](#addText-java.lang.String-) | Adds a plain text to the argument. |
| [addNode(Inline node)](#addNode-com.aspose.words.Inline-) | Adds a node to the argument. |
| [addField(FieldBuilder fieldBuilder)](#addField-com.aspose.words.FieldBuilder-) | Adds a field represented by a [FieldBuilder](../../com.aspose.words/fieldbuilder) to the argument. |
| [buildBlock(DocumentBuilder documentBuilder)](#buildBlock-com.aspose.words.DocumentBuilder-) |  |
### FieldArgumentBuilder() {#FieldArgumentBuilder--}
```
public FieldArgumentBuilder()
```


Initializes an instance of the [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder) class.

### addText(String text) {#addText-java.lang.String-}
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
### addNode(Inline node) {#addNode-com.aspose.words.Inline-}
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
### addField(FieldBuilder fieldBuilder) {#addField-com.aspose.words.FieldBuilder-}
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
### buildBlock(DocumentBuilder documentBuilder) {#buildBlock-com.aspose.words.DocumentBuilder-}
```
public void buildBlock(DocumentBuilder documentBuilder)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentBuilder | [DocumentBuilder](../../com.aspose.words/documentbuilder) |  |

