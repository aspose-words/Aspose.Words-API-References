---
title: FieldBuilder
second_title: Aspose.Words for Java API Reference
description: Builds a field from field code tokens arguments and switches.
type: docs
weight: 166
url: /java/com.aspose.words/fieldbuilder/
---

**Inheritance:**
java.lang.Object
```
public class FieldBuilder
```

Builds a field from field code tokens (arguments and switches).

To learn more, visit the **Working with Fields** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [FieldBuilder(int fieldType)](#FieldBuilder-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [addArgument(String argument)](#addArgument-java.lang.String-) | Adds a field's argument. |
| [addArgument(int argument)](#addArgument-int-) | Adds a field's argument. |
| [addArgument(double argument)](#addArgument-double-) | Adds a field's argument. |
| [addArgument(FieldBuilder argument)](#addArgument-com.aspose.words.FieldBuilder-) | Adds a child field represented by another [FieldBuilder](../../com.aspose.words/fieldbuilder) to the field's code. |
| [addArgument(FieldArgumentBuilder argument)](#addArgument-com.aspose.words.FieldArgumentBuilder-) | Adds a field's argument represented by [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder) to the field's code. |
| [addSwitch(String switchName)](#addSwitch-java.lang.String-) | Adds a field's switch. |
| [addSwitch(String switchName, String switchArgument)](#addSwitch-java.lang.String-java.lang.String-) | Adds a field's switch. |
| [addSwitch(String switchName, int switchArgument)](#addSwitch-java.lang.String-int-) | Adds a field's switch. |
| [addSwitch(String switchName, double switchArgument)](#addSwitch-java.lang.String-double-) | Adds a field's switch. |
| [buildAndInsert(Inline refNode)](#buildAndInsert-com.aspose.words.Inline-) | Builds and inserts a field into the document before the specified inline node. |
| [buildAndInsert(Paragraph refNode)](#buildAndInsert-com.aspose.words.Paragraph-) | Builds and inserts a field into the document to the end of the specified paragraph. |
| [buildBlock(DocumentBuilder documentBuilder)](#buildBlock-com.aspose.words.DocumentBuilder-) |  |
### FieldBuilder(int fieldType) {#FieldBuilder-int-}
```
public FieldBuilder(int fieldType)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | int |  |

### addArgument(String argument) {#addArgument-java.lang.String-}
```
public FieldBuilder addArgument(String argument)
```


Adds a field's argument.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| argument | java.lang.String | The argument value. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addArgument(int argument) {#addArgument-int-}
```
public FieldBuilder addArgument(int argument)
```


Adds a field's argument.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| argument | int | The argument value. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addArgument(double argument) {#addArgument-double-}
```
public FieldBuilder addArgument(double argument)
```


Adds a field's argument.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| argument | double | The argument value. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addArgument(FieldBuilder argument) {#addArgument-com.aspose.words.FieldBuilder-}
```
public FieldBuilder addArgument(FieldBuilder argument)
```


Adds a child field represented by another [FieldBuilder](../../com.aspose.words/fieldbuilder) to the field's code. This overload is used when the argument consists of a single child field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| argument | [FieldBuilder](../../com.aspose.words/fieldbuilder) |  |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addArgument(FieldArgumentBuilder argument) {#addArgument-com.aspose.words.FieldArgumentBuilder-}
```
public FieldBuilder addArgument(FieldArgumentBuilder argument)
```


Adds a field's argument represented by [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder) to the field's code. This overload is used when the argument consists of a mixture of different parts such as child fields, nodes, and plain text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| argument | [FieldArgumentBuilder](../../com.aspose.words/fieldargumentbuilder) |  |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addSwitch(String switchName) {#addSwitch-java.lang.String-}
```
public FieldBuilder addSwitch(String switchName)
```


Adds a field's switch. This overload adds a flag (switch without argument).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String | The switch name. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addSwitch(String switchName, String switchArgument) {#addSwitch-java.lang.String-java.lang.String-}
```
public FieldBuilder addSwitch(String switchName, String switchArgument)
```


Adds a field's switch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String | The switch name. |
| switchArgument | java.lang.String | The switch value. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addSwitch(String switchName, int switchArgument) {#addSwitch-java.lang.String-int-}
```
public FieldBuilder addSwitch(String switchName, int switchArgument)
```


Adds a field's switch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String | The switch name. |
| switchArgument | int | The switch value. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### addSwitch(String switchName, double switchArgument) {#addSwitch-java.lang.String-double-}
```
public FieldBuilder addSwitch(String switchName, double switchArgument)
```


Adds a field's switch.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String | The switch name. |
| switchArgument | double | The switch value. |

**Returns:**
[FieldBuilder](../../com.aspose.words/fieldbuilder)
### buildAndInsert(Inline refNode) {#buildAndInsert-com.aspose.words.Inline-}
```
public Field buildAndInsert(Inline refNode)
```


Builds and inserts a field into the document before the specified inline node.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| refNode | [Inline](../../com.aspose.words/inline) |  |

**Returns:**
[Field](../../com.aspose.words/field) - A [Field](../../com.aspose.words/field) object that represents the inserted field.
### buildAndInsert(Paragraph refNode) {#buildAndInsert-com.aspose.words.Paragraph-}
```
public Field buildAndInsert(Paragraph refNode)
```


Builds and inserts a field into the document to the end of the specified paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| refNode | [Paragraph](../../com.aspose.words/paragraph) |  |

**Returns:**
[Field](../../com.aspose.words/field) - A [Field](../../com.aspose.words/field) object that represents the inserted field.
### buildBlock(DocumentBuilder documentBuilder) {#buildBlock-com.aspose.words.DocumentBuilder-}
```
public void buildBlock(DocumentBuilder documentBuilder)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentBuilder | [DocumentBuilder](../../com.aspose.words/documentbuilder) |  |

