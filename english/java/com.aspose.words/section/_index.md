---
title: Section
second_title: Aspose.Words for Java API Reference
description: Represents a single section in a document.
type: docs
weight: 509
url: /java/com.aspose.words/section/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class Section extends CompositeNode
```

Represents a single section in a document.

To learn more, visit the **Working with Sections** documentation article.

**Section** can have one [getBody()](../../com.aspose.words/section\#getBody--) and maximum one [HeaderFooter](../../com.aspose.words/headerfooter) of each [HeaderFooterType](../../com.aspose.words/headerfootertype). **Body** and **HeaderFooter** nodes can be in any order inside **Section**.

A minimal valid section needs to have **Body** with one **Paragraph**.

Each section has its own set of properties that specify page size, orientation, margins etc.

You can create a copy of a section using [Node.deepClone(boolean)](../../com.aspose.words/node\#deepClone-boolean-). The copy can be inserted into the same or different document.

To add, insert or remove a whole section including section break and section properties use methods of the **Sections** object.

To copy and insert just content of the section excluding the section break and section properties use **AppendContent** and **PrependContent** methods.
## Constructors

| Constructor | Description |
| --- | --- |
| [Section(DocumentBase doc)](#Section-com.aspose.words.DocumentBase-) | Initializes a new instance of the Section class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns **NodeType.Section**. |
| [getBody()](#getBody--) | Returns the **Body** child node of the section. |
| [getHeadersFooters()](#getHeadersFooters--) | Provides access to the headers and footers nodes of the section. |
| [getPageSetup()](#getPageSetup--) | Returns an object that represents page setup and section properties. |
| [getProtectedForForms()](#getProtectedForForms--) | True if the section is protected for forms. |
| [setProtectedForForms(boolean value)](#setProtectedForForms-boolean-) | True if the section is protected for forms. |
| [deepClone()](#deepClone--) | Creates a duplicate of this section. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [prependContent(Section sourceSection)](#prependContent-com.aspose.words.Section-) | Inserts a copy of content of the source section at the beginning of this section. |
| [appendContent(Section sourceSection)](#appendContent-com.aspose.words.Section-) | Inserts a copy of content of the source section at the end of this section. |
| [clearContent()](#clearContent--) | Clears the section. |
| [clearHeadersFooters()](#clearHeadersFooters--) | Clears the headers and footers of this section. |
| [deleteHeaderFooterShapes()](#deleteHeaderFooterShapes--) | Deletes all shapes (drawing objects) from the headers and footers of this section. |
| [ensureMinimum()](#ensureMinimum--) | Ensures that the section has Body with one Paragraph. |
| [getDirectSectionAttr(int key)](#getDirectSectionAttr-int-) |  |
| [fetchInheritedSectionAttr(int key)](#fetchInheritedSectionAttr-int-) |  |
| [fetchSectionAttr(int key)](#fetchSectionAttr-int-) |  |
| [setSectionAttr(int key, Object value)](#setSectionAttr-int-java.lang.Object-) |  |
| [clearSectionAttrs()](#clearSectionAttrs--) |  |
| [toString()](#toString--) |  |
### Section(DocumentBase doc) {#Section-com.aspose.words.DocumentBase-}
```
public Section(DocumentBase doc)
```


Initializes a new instance of the Section class.

When the section is created, it belongs to the specified document, but is not yet part of the document and **ParentNode** is null.

To include Section into a document use Document.InsertAfter, Document.InsertBefore or Sections.Add and Section.Insert methods.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.Section**.

**Returns:**
int - **NodeType.Section**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getBody() {#getBody--}
```
public Body getBody()
```


Returns the **Body** child node of the section.

**Body** contains main text of the section.

Returns null if the section does not have a **Body** node among its children.

**Returns:**
[Body](../../com.aspose.words/body) - The **Body** child node of the section.
### getHeadersFooters() {#getHeadersFooters--}
```
public HeaderFooterCollection getHeadersFooters()
```


Provides access to the headers and footers nodes of the section.

**Returns:**
[HeaderFooterCollection](../../com.aspose.words/headerfootercollection) - The corresponding [HeaderFooterCollection](../../com.aspose.words/headerfootercollection) value.
### getPageSetup() {#getPageSetup--}
```
public PageSetup getPageSetup()
```


Returns an object that represents page setup and section properties.

**Returns:**
[PageSetup](../../com.aspose.words/pagesetup) - An object that represents page setup and section properties.
### getProtectedForForms() {#getProtectedForForms--}
```
public boolean getProtectedForForms()
```


True if the section is protected for forms. When a section is protected for forms, users can select and modify text only in form fields in Microsoft Word.

**Returns:**
boolean - The corresponding  boolean  value.
### setProtectedForForms(boolean value) {#setProtectedForForms-boolean-}
```
public void setProtectedForForms(boolean value)
```


True if the section is protected for forms. When a section is protected for forms, users can select and modify text only in form fields in Microsoft Word.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### deepClone() {#deepClone--}
```
public Section deepClone()
```


Creates a duplicate of this section.

**Returns:**
[Section](../../com.aspose.words/section)
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Enumerates over this node and all of its children. Each node calls a corresponding method on DocumentVisitor.

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls DocumentVisitor.VisitSectionStart, then calls Accept for all child nodes of the section and calls DocumentVisitor.VisitSectionEnd at the end.
### prependContent(Section sourceSection) {#prependContent-com.aspose.words.Section-}
```
public void prependContent(Section sourceSection)
```


Inserts a copy of content of the source section at the beginning of this section.

Only content of [getBody()](../../com.aspose.words/section\#getBody--) of the source section is copied, page setup, headers and footers are not copied.

The nodes are automatically imported if the source section belongs to a different document.

No new section is created in the destination document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceSection | [Section](../../com.aspose.words/section) | The section to copy content from. |

### appendContent(Section sourceSection) {#appendContent-com.aspose.words.Section-}
```
public void appendContent(Section sourceSection)
```


Inserts a copy of content of the source section at the end of this section.

Only content of [getBody()](../../com.aspose.words/section\#getBody--) of the source section is copied, page setup, headers and footers are not copied.

The nodes are automatically imported if the source section belongs to a different document.

No new section is created in the destination document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceSection | [Section](../../com.aspose.words/section) | The section to copy content from. |

### clearContent() {#clearContent--}
```
public void clearContent()
```


Clears the section.

The text of [getBody()](../../com.aspose.words/section\#getBody--) is cleared, only one empty paragraph is left that represents the section break.

The text of all headers and footers is cleared, but [HeaderFooter](../../com.aspose.words/headerfooter) objects themselves are not removed.

### clearHeadersFooters() {#clearHeadersFooters--}
```
public void clearHeadersFooters()
```


Clears the headers and footers of this section.

The text of all headers and footers is cleared, but [HeaderFooter](../../com.aspose.words/headerfooter) objects themselves are not removed.

This makes headers and footers of this section linked to headers and footers of the previous section.

### deleteHeaderFooterShapes() {#deleteHeaderFooterShapes--}
```
public void deleteHeaderFooterShapes()
```


Deletes all shapes (drawing objects) from the headers and footers of this section.

### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


Ensures that the section has Body with one Paragraph.

### getDirectSectionAttr(int key) {#getDirectSectionAttr-int-}
```
public Object getDirectSectionAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedSectionAttr(int key) {#fetchInheritedSectionAttr-int-}
```
public Object fetchInheritedSectionAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchSectionAttr(int key) {#fetchSectionAttr-int-}
```
public Object fetchSectionAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setSectionAttr(int key, Object value) {#setSectionAttr-int-java.lang.Object-}
```
public void setSectionAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### clearSectionAttrs() {#clearSectionAttrs--}
```
public void clearSectionAttrs()
```




### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
