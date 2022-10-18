---
title: Revision
second_title: Aspose.Words for Java API Reference
description: Represents a revision tracked change in a document node or style.
type: docs
weight: 483
url: /java/com.aspose.words/revision/
---

**Inheritance:**
java.lang.Object
```
public class Revision
```

Represents a revision (tracked change) in a document node or style. Use [getRevisionType()](../../com.aspose.words/revision\#getRevisionType--) to check the type of this revision.

To learn more, visit the **Track Changes in a Document** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [accept()](#accept--) | Accepts this revision. |
| [reject()](#reject--) | Reject this revision. |
| [getAuthor()](#getAuthor--) | Gets the author of this revision. |
| [setAuthor(String value)](#setAuthor-java.lang.String-) | Sets the author of this revision. |
| [getDateTime()](#getDateTime--) | Gets the date/time of this revision. |
| [setDateTime(Date value)](#setDateTime-java.util.Date-) | Sets the date/time of this revision. |
| [getRevisionType()](#getRevisionType--) | Gets the type of this revision. |
| [getParentNode()](#getParentNode--) | Gets the immediate parent node (owner) of this revision. |
| [getParentStyle()](#getParentStyle--) | Gets the immediate parent style (owner) of this revision. |
| [getGroup()](#getGroup--) | Gets the revision group. |
### accept() {#accept--}
```
public void accept()
```


Accepts this revision.

### reject() {#reject--}
```
public void reject()
```


Reject this revision.

### getAuthor() {#getAuthor--}
```
public String getAuthor()
```


Gets the author of this revision. Can not be empty string or null.

**Returns:**
java.lang.String - The author of this revision.
### setAuthor(String value) {#setAuthor-java.lang.String-}
```
public void setAuthor(String value)
```


Sets the author of this revision. Can not be empty string or null.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The author of this revision. |

### getDateTime() {#getDateTime--}
```
public Date getDateTime()
```


Gets the date/time of this revision.

**Returns:**
java.util.Date - The date/time of this revision.
### setDateTime(Date value) {#setDateTime-java.util.Date-}
```
public void setDateTime(Date value)
```


Sets the date/time of this revision.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date | The date/time of this revision. |

### getRevisionType() {#getRevisionType--}
```
public int getRevisionType()
```


Gets the type of this revision.

**Returns:**
int - The type of this revision. The returned value is one of [RevisionType](../../com.aspose.words/revisiontype) constants.
### getParentNode() {#getParentNode--}
```
public Node getParentNode()
```


Gets the immediate parent node (owner) of this revision. This property will work for any revision type other than [RevisionType.STYLE\_DEFINITION\_CHANGE](../../com.aspose.words/revisiontype\#STYLE-DEFINITION-CHANGE). If this revision relates to change of Style formatting, use [getParentStyle()](../../com.aspose.words/revision\#getParentStyle--) instead.

**Returns:**
[Node](../../com.aspose.words/node) - The immediate parent node (owner) of this revision.
### getParentStyle() {#getParentStyle--}
```
public Style getParentStyle()
```


Gets the immediate parent style (owner) of this revision. This property will work for only for the [RevisionType.STYLE\_DEFINITION\_CHANGE](../../com.aspose.words/revisiontype\#STYLE-DEFINITION-CHANGE) revision type. If this revision relates to changes on document nodes, use [getParentNode()](../../com.aspose.words/revision\#getParentNode--) instead.

**Returns:**
[Style](../../com.aspose.words/style) - The immediate parent style (owner) of this revision.
### getGroup() {#getGroup--}
```
public RevisionGroup getGroup()
```


Gets the revision group. Returns null if the revision does not belong to any group. Revision has no group if revision type is RevisionType.StyleDefinitionChange or if the revision is not longer exist in document context (accepted/rejected).

**Returns:**
[RevisionGroup](../../com.aspose.words/revisiongroup) - The revision group.
