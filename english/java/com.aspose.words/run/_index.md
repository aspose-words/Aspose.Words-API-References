---
title: Run
second_title: Aspose.Words for Java API Reference
description: Represents a run of characters with the same font formatting.
type: docs
weight: 497
url: /java/com.aspose.words/run/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.Inline](../../com.aspose.words/inline)
```
public class Run extends Inline
```

Represents a run of characters with the same font formatting.

To learn more, visit the **Programming with Documents** documentation article.

All text of the document is stored in runs of text.

**Run** can only be a child of **Paragraph** or inline **StructuredDocumentTag**.
## Constructors

| Constructor | Description |
| --- | --- |
| [Run(DocumentBase doc)](#Run-com.aspose.words.DocumentBase-) | Initializes a new instance of the **Run** class. |
| [Run(DocumentBase doc, String text)](#Run-com.aspose.words.DocumentBase-java.lang.String-) | Initializes a new instance of the **Run** class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns **NodeType.Run**. |
| [getText()](#getText--) | Gets the text of the run. |
| [setText(String value)](#setText-java.lang.String-) | Sets the text of the run. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
### Run(DocumentBase doc) {#Run-com.aspose.words.DocumentBase-}
```
public Run(DocumentBase doc)
```


Initializes a new instance of the **Run** class.

When **Run** is created, it belongs to the specified document, but is not yet part of the document and **ParentNode** is null.

To append **Run** to the document use InsertAfter or InsertBefore on the paragraph where you want the run inserted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |

### Run(DocumentBase doc, String text) {#Run-com.aspose.words.DocumentBase-java.lang.String-}
```
public Run(DocumentBase doc, String text)
```


Initializes a new instance of the **Run** class.

When **Run** is created, it belongs to the specified document, but is not yet part of the document and **ParentNode** is null.

To append **Run** to the document use InsertAfter or InsertBefore on the paragraph where you want the run inserted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |
| text | java.lang.String | The text of the run. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.Run**.

**Returns:**
int - **NodeType.Run**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getText() {#getText--}
```
public String getText()
```


Gets the text of the run.

**Returns:**
java.lang.String - The text of the run.
### setText(String value) {#setText-java.lang.String-}
```
public void setText(String value)
```


Sets the text of the run.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text of the run. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Calls DocumentVisitor.VisitRun.

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the node. |

**Returns:**
boolean - False if the visitor requested the enumeration to stop.
