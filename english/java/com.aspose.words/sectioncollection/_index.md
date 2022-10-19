---
title: SectionCollection
second_title: Aspose.Words for Java API Reference
description: A collection of Section objects in the document.
type: docs
weight: 510
url: /java/com.aspose.words/sectioncollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection)
```
public class SectionCollection extends NodeCollection
```

A collection of **Section** objects in the document.

To learn more, visit the **Working with Sections** documentation article.

A Microsoft Word document can contain multiple sections. To create a section in a Microsoft Word, select the Insert/Break command and select a break type. The break specifies whether section starts on a new page or on the same page.

Programmatically inserting and removing sections can be used to customize documents produced during mail merge. If a document needs to have different content or parts of the content depending on some criteria, then you can create a "master" document that contains multiple sections and delete some of the sections before or after mail merge.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int-) | Retrieves a section at the given index. |
| [toArray()](#toArray--) | Copies all sections from the collection to a new array of sections. |
### get(int index) {#get-int-}
```
public Node get(int index)
```


Retrieves a section at the given index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the list of sections. |

**Returns:**
[Node](../../com.aspose.words/node) - The corresponding [Section](../../com.aspose.words/section) value.
### toArray() {#toArray--}
```
public Node[] toArray()
```


Copies all sections from the collection to a new array of sections.

**Returns:**
com.aspose.words.Node[] - An array of sections.
