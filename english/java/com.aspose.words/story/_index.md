---
title: Story
second_title: Aspose.Words for Java API Reference
description: Base class for elements that contain block-level nodes  and .
type: docs
weight: 528
url: /java/com.aspose.words/story/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public abstract class Story extends CompositeNode
```

Base class for elements that contain block-level nodes [Paragraph](../../com.aspose.words/paragraph) and [Table](../../com.aspose.words/table).

To learn more, visit the **Logical Levels of Nodes in a Document** documentation article.

Text of a Word document is said to consist of several stories. The main text is stored in the main text story represented by [Body](../../com.aspose.words/body), each header and footer is stored in a separate story represented by [HeaderFooter](../../com.aspose.words/headerfooter).
## Constructors

| Constructor | Description |
| --- | --- |
| [Story()](#Story--) |  |
## Methods

| Method | Description |
| --- | --- |
| [getStoryType()](#getStoryType--) | Gets the type of this story. |
| [getFirstParagraph()](#getFirstParagraph--) | Gets the first paragraph in the story. |
| [getLastParagraph()](#getLastParagraph--) | Gets the last paragraph in the story. |
| [getParagraphs()](#getParagraphs--) | Gets a collection of paragraphs that are immediate children of the story. |
| [getTables()](#getTables--) | Gets a collection of tables that are immediate children of the story. |
| [deleteShapes()](#deleteShapes--) | Deletes all shapes from the text of this story. |
| [appendParagraph(String text)](#appendParagraph-java.lang.String-) | A shortcut method that creates a [Paragraph](../../com.aspose.words/paragraph) object with optional text and appends it to the end of this object. |
### Story() {#Story--}
```
public Story()
```


### getStoryType() {#getStoryType--}
```
public int getStoryType()
```


Gets the type of this story.

**Returns:**
int - The type of this story. The returned value is one of [StoryType](../../com.aspose.words/storytype) constants.
### getFirstParagraph() {#getFirstParagraph--}
```
public Paragraph getFirstParagraph()
```


Gets the first paragraph in the story.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The first paragraph in the story.
### getLastParagraph() {#getLastParagraph--}
```
public Paragraph getLastParagraph()
```


Gets the last paragraph in the story.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The last paragraph in the story.
### getParagraphs() {#getParagraphs--}
```
public ParagraphCollection getParagraphs()
```


Gets a collection of paragraphs that are immediate children of the story.

**Returns:**
[ParagraphCollection](../../com.aspose.words/paragraphcollection) - A collection of paragraphs that are immediate children of the story.
### getTables() {#getTables--}
```
public TableCollection getTables()
```


Gets a collection of tables that are immediate children of the story.

**Returns:**
[TableCollection](../../com.aspose.words/tablecollection) - A collection of tables that are immediate children of the story.
### deleteShapes() {#deleteShapes--}
```
public void deleteShapes()
```


Deletes all shapes from the text of this story.

### appendParagraph(String text) {#appendParagraph-java.lang.String-}
```
public Paragraph appendParagraph(String text)
```


A shortcut method that creates a [Paragraph](../../com.aspose.words/paragraph) object with optional text and appends it to the end of this object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String | The text for the paragraph. Can be null or empty string. |

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The newly created and appended paragraph.
