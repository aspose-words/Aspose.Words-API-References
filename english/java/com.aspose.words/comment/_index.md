---
title: Comment
second_title: Aspose.Words for Java API Reference
description: Represents a container for text of a comment.
type: docs
weight: 76
url: /java/com.aspose.words/comment/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.InlineStory](../../com.aspose.words/inlinestory)
```
public class Comment extends InlineStory
```

Represents a container for text of a comment.

To learn more, visit the **Working with Comments** documentation article.

A comment is an annotation which is anchored to a region of text or to a position in text. A comment can contain an arbitrary amount of block-level content.

If a [Comment](../../com.aspose.words/comment) object occurs on its own, the comment is anchored to the position of the [Comment](../../com.aspose.words/comment) object.

To anchor a comment to a region of text three objects are required: [Comment](../../com.aspose.words/comment), [CommentRangeStart](../../com.aspose.words/commentrangestart) and [CommentRangeEnd](../../com.aspose.words/commentrangeend). All three objects need to share the same [getId()](../../com.aspose.words/comment\#getId--) value.

[Comment](../../com.aspose.words/comment) is an inline-level node and can only be a child of [Paragraph](../../com.aspose.words/paragraph).

[Comment](../../com.aspose.words/comment) can contain [Paragraph](../../com.aspose.words/paragraph) and [Table](../../com.aspose.words/table) child nodes.
## Constructors

| Constructor | Description |
| --- | --- |
| [Comment(DocumentBase doc)](#Comment-com.aspose.words.DocumentBase-) | Initializes a new instance of the **Comment** class. |
| [Comment(DocumentBase doc, String author, String initial, Date dateTime)](#Comment-com.aspose.words.DocumentBase-java.lang.String-java.lang.String-java.util.Date-) | Initializes a new instance of the **Comment** class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns **NodeType.Comment**. |
| [getStoryType()](#getStoryType--) | Returns **StoryType.Comments**. |
| [getId()](#getId--) | Gets the comment identifier. |
| [getIdInternal()](#getIdInternal--) |  |
| [setIdInternal(int value)](#setIdInternal-int-) |  |
| [getParentIdInternal()](#getParentIdInternal--) |  |
| [setParentIdInternal(int value)](#setParentIdInternal-int-) |  |
| [getInitial()](#getInitial--) | Gets the initials of the user associated with a specific comment. |
| [setInitial(String value)](#setInitial-java.lang.String-) | Sets the initials of the user associated with a specific comment. |
| [getDateTime()](#getDateTime--) | Gets the date and time that the comment was made. |
| [setDateTime(Date value)](#setDateTime-java.util.Date-) | Gets the date and time that the comment was made. |
| [getAuthor()](#getAuthor--) | Gets the author name for a comment. |
| [setAuthor(String value)](#setAuthor-java.lang.String-) | Sets the author name for a comment. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [addReply(String author, String initial, Date dateTime, String text)](#addReply-java.lang.String-java.lang.String-java.util.Date-java.lang.String-) | Adds a reply to this comment. |
| [removeReply(Comment reply)](#removeReply-com.aspose.words.Comment-) | Removes the specified reply to this comment. |
| [removeAllReplies()](#removeAllReplies--) | Removes all replies to this comment. |
| [setText(String text)](#setText-java.lang.String-) | This is a convenience method that allows to easily set text of the comment. |
| [getAncestor()](#getAncestor--) | Returns the parent Comment object. |
| [getReplies()](#getReplies--) | Returns a collection of [Comment](../../com.aspose.words/comment) objects that are immediate children of the specified comment. |
| [getDone()](#getDone--) | Gets flag indicating that the comment has been marked done. |
| [setDone(boolean value)](#setDone-boolean-) | Sets flag indicating that the comment has been marked done. |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
### Comment(DocumentBase doc) {#Comment-com.aspose.words.DocumentBase-}
```
public Comment(DocumentBase doc)
```


Initializes a new instance of the **Comment** class.

When **Comment** is created, it belongs to the specified document, but is not yet part of the document and **ParentNode** is null.

To append **Comment** to the document use InsertAfter or InsertBefore on the paragraph where you want the comment inserted.

After creating a comment, don't forget to set its [getAuthor()](../../com.aspose.words/comment\#getAuthor--) / [setAuthor(java.lang.String)](../../com.aspose.words/comment\#setAuthor-java.lang.String-), [getInitial()](../../com.aspose.words/comment\#getInitial--) / [setInitial(java.lang.String)](../../com.aspose.words/comment\#setInitial-java.lang.String-) and [getDateTime()](../../com.aspose.words/comment\#getDateTime--) / [setDateTime(java.util.Date)](../../com.aspose.words/comment\#setDateTime-java.util.Date-) properties.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |

### Comment(DocumentBase doc, String author, String initial, Date dateTime) {#Comment-com.aspose.words.DocumentBase-java.lang.String-java.lang.String-java.util.Date-}
```
public Comment(DocumentBase doc, String author, String initial, Date dateTime)
```


Initializes a new instance of the **Comment** class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |
| author | java.lang.String | The author name for the comment. Cannot be null. |
| initial | java.lang.String | The author initials for the comment. Cannot be null. |
| dateTime | java.util.Date | The date and time for the comment. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.Comment**.

**Returns:**
int - **NodeType.Comment**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getStoryType() {#getStoryType--}
```
public int getStoryType()
```


Returns **StoryType.Comments**.

**Returns:**
int - **StoryType.Comments**. The returned value is one of [StoryType](../../com.aspose.words/storytype) constants.
### getId() {#getId--}
```
public int getId()
```


Gets the comment identifier.

The comment identifier allows to anchor a comment to a region of text in the document. The region must be demarcated using the [CommentRangeStart](../../com.aspose.words/commentrangestart) and [CommentRangeEnd](../../com.aspose.words/commentrangeend) object sharing the same identifier value as the [Comment](../../com.aspose.words/comment) object.

You would use this value when looking for the [CommentRangeStart](../../com.aspose.words/commentrangestart) and [CommentRangeEnd](../../com.aspose.words/commentrangeend) nodes that are linked to this comment.

Comment identifiers are supposed to be unique across a document and Aspose.Words automatically maintains comment identifiers when loading, saving and combining documents.

**Returns:**
int - The comment identifier.
### getIdInternal() {#getIdInternal--}
```
public int getIdInternal()
```




**Returns:**
int
### setIdInternal(int value) {#setIdInternal-int-}
```
public void setIdInternal(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getParentIdInternal() {#getParentIdInternal--}
```
public int getParentIdInternal()
```




**Returns:**
int
### setParentIdInternal(int value) {#setParentIdInternal-int-}
```
public void setParentIdInternal(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getInitial() {#getInitial--}
```
public String getInitial()
```


Gets the initials of the user associated with a specific comment.

Cannot be null.

Default is empty string.

**Returns:**
java.lang.String - The initials of the user associated with a specific comment.
### setInitial(String value) {#setInitial-java.lang.String-}
```
public void setInitial(String value)
```


Sets the initials of the user associated with a specific comment.

Cannot be null.

Default is empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The initials of the user associated with a specific comment. |

### getDateTime() {#getDateTime--}
```
public Date getDateTime()
```


Gets the date and time that the comment was made.

Default is 03.01.0001.

**Returns:**
java.util.Date - The date and time that the comment was made.
### setDateTime(Date value) {#setDateTime-java.util.Date-}
```
public void setDateTime(Date value)
```


Gets the date and time that the comment was made.

Default is 03.01.0001.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date | The date and time that the comment was made. |

### getAuthor() {#getAuthor--}
```
public String getAuthor()
```


Gets the author name for a comment.

Cannot be null.

Default is empty string.

**Returns:**
java.lang.String - The author name for a comment.
### setAuthor(String value) {#setAuthor-java.lang.String-}
```
public void setAuthor(String value)
```


Sets the author name for a comment.

Cannot be null.

Default is empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The author name for a comment. |

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
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls [DocumentVisitor.visitCommentStart(com.aspose.words.Comment)](../../com.aspose.words/documentvisitor\#visitCommentStart-com.aspose.words.Comment-), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) for all child nodes of the comment and calls [DocumentVisitor.visitCommentEnd(com.aspose.words.Comment)](../../com.aspose.words/documentvisitor\#visitCommentEnd-com.aspose.words.Comment-) at the end.
### addReply(String author, String initial, Date dateTime, String text) {#addReply-java.lang.String-java.lang.String-java.util.Date-java.lang.String-}
```
public Comment addReply(String author, String initial, Date dateTime, String text)
```


Adds a reply to this comment.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| author | java.lang.String | The author name for the reply. |
| initial | java.lang.String | The author initials for the reply. |
| dateTime | java.util.Date | The date and time for the reply. |
| text | java.lang.String | The reply text. |

**Returns:**
[Comment](../../com.aspose.words/comment) - The created [Comment](../../com.aspose.words/comment) node for the reply. Due to the existing MS Office limitations only 1 level of replies is allowed in the document. An exception of type java.lang.IllegalStateException will be raised if this method is called on the existing Reply comment.
### removeReply(Comment reply) {#removeReply-com.aspose.words.Comment-}
```
public void removeReply(Comment reply)
```


Removes the specified reply to this comment. All constituent nodes of the reply will be deleted from the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| reply | [Comment](../../com.aspose.words/comment) | The comment node of the deleting reply. |

### removeAllReplies() {#removeAllReplies--}
```
public void removeAllReplies()
```


Removes all replies to this comment. All constituent nodes of the replies will be deleted from the document.

### setText(String text) {#setText-java.lang.String-}
```
public void setText(String text)
```


This is a convenience method that allows to easily set text of the comment.

This method allows to quickly set text of a comment from a string. The string can contain paragraph breaks, this will create paragraphs of text in the comment accordingly. If you want to insert more complex elements into the comment, for example bookmarks or tables or apply rich formatting, then you need to use the appropriate node classes to build up the comment text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String | The new text of the comment. |

### getAncestor() {#getAncestor--}
```
public Comment getAncestor()
```


Returns the parent Comment object. Returns null for top-level comments.

**Returns:**
[Comment](../../com.aspose.words/comment) - The parent Comment object.
### getReplies() {#getReplies--}
```
public CommentCollection getReplies()
```


Returns a collection of [Comment](../../com.aspose.words/comment) objects that are immediate children of the specified comment.

**Returns:**
[CommentCollection](../../com.aspose.words/commentcollection) - A collection of [Comment](../../com.aspose.words/comment) objects that are immediate children of the specified comment.
### getDone() {#getDone--}
```
public boolean getDone()
```


Gets flag indicating that the comment has been marked done.

**Returns:**
boolean - Flag indicating that the comment has been marked done.
### setDone(boolean value) {#setDone-boolean-}
```
public void setDone(boolean value)
```


Sets flag indicating that the comment has been marked done.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Flag indicating that the comment has been marked done. |

### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




