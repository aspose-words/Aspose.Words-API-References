---
title: HeaderFooterCollection
second_title: Aspose.Words for Java API Reference
description: Provides typed access to  nodes of a Section.
type: docs
weight: 317
url: /java/com.aspose.words/headerfootercollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection)
```
public class HeaderFooterCollection extends NodeCollection
```

Provides typed access to [HeaderFooter](../../com.aspose.words/headerfooter) nodes of a **Section**.

To learn more, visit the **Working with Headers and Footers** documentation article.

There can be maximum of one **HeaderFooter**

of each [HeaderFooterType](../../com.aspose.words/headerfootertype) per **Section**.

**HeaderFooter** objects can occur in any order in the collection.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int-) | Retrieves a **HeaderFooter** at the given index. |
| [getByHeaderFooterType(int headerFooterType)](#getByHeaderFooterType-int-) |  |
| [linkToPrevious(boolean isLinkToPrevious)](#linkToPrevious-boolean-) | Links or unlinks all headers and footers to the corresponding headers and footers in the previous section. |
| [linkToPrevious(int headerFooterType, boolean isLinkToPrevious)](#linkToPrevious-int-boolean-) |  |
| [toArray()](#toArray--) | Copies all  HeaderFoorter  s from the collection to a new array of  HeaderFoorter  s. |
### get(int index) {#get-int-}
```
public Node get(int index)
```


Retrieves a **HeaderFooter** at the given index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Node](../../com.aspose.words/node) - The corresponding [HeaderFooter](../../com.aspose.words/headerfooter) value.
### getByHeaderFooterType(int headerFooterType) {#getByHeaderFooterType-int-}
```
public HeaderFooter getByHeaderFooterType(int headerFooterType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
[HeaderFooter](../../com.aspose.words/headerfooter)
### linkToPrevious(boolean isLinkToPrevious) {#linkToPrevious-boolean-}
```
public void linkToPrevious(boolean isLinkToPrevious)
```


Links or unlinks all headers and footers to the corresponding headers and footers in the previous section.

If any of the headers or footers do not exist, creates them automatically.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| isLinkToPrevious | boolean | True to link the headers and footers to the previous section; false to unlink them. |

### linkToPrevious(int headerFooterType, boolean isLinkToPrevious) {#linkToPrevious-int-boolean-}
```
public void linkToPrevious(int headerFooterType, boolean isLinkToPrevious)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |
| isLinkToPrevious | boolean |  |

### toArray() {#toArray--}
```
public HeaderFooter[] toArray()
```


Copies all  HeaderFoorter  s from the collection to a new array of  HeaderFoorter  s.

**Returns:**
com.aspose.words.HeaderFooter[] - An array of  HeaderFoorter  s.
