---
title: DocumentBuilder.moveToStructuredDocumentTag method
linktitle: moveToStructuredDocumentTag method
articleTitle: moveToStructuredDocumentTag method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.DocumentBuilder.moveToStructuredDocumentTag method"
type: docs
weight: 620
url: /nodejs-net/aspose.words/documentbuilder/moveToStructuredDocumentTag/
---

## moveToStructuredDocumentTag(structuredDocumentTagIndex, characterIndex) {#number_number}

Moves the cursor to a structured document tag in the current section.


```js
moveToStructuredDocumentTag(structuredDocumentTagIndex: number, characterIndex: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| structuredDocumentTagIndex | number | The index of the structured document tag to move to. |
| characterIndex | number | The index of the character inside the structured document tag. A negative value allows you to specify a position from the end of the structured document tag. Use -1 to move to the end of the structured document tag. If the structured document tag is at the block level, and you want to move the cursor to the end of its last paragraph, specify -2. |

### Remarks

The navigation is performed inside the current story of the current section. That is, if you moved the
cursor to the primary header of the first section, then *structuredDocumentTagIndex*
specified the index of the structured document tag inside that header of that section.

When *structuredDocumentTagIndex* is greater than or equal to 0, it specifies an index
from the beginning of the section with 0 being the first structured document tag. When*structuredDocumentTagIndex* is less than 0, it specified an index from the end of the
section with -1 being the last structured document tag.




## moveToStructuredDocumentTag(structuredDocumentTag, characterIndex) {#structureddocumenttag_number}

Moves the cursor to the structured document tag.


```js
moveToStructuredDocumentTag(structuredDocumentTag: Aspose.Words.Markup.StructuredDocumentTag, characterIndex: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| structuredDocumentTag | [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) | The structured document tag to move to. |
| characterIndex | number | The index of the character inside the structured document tag. A negative value allows you to specify a position from the end of the structured document tag. Use -1 to move to the end of the structured document tag. If the structured document tag is at the block level, and you want to move the cursor to the end of its last paragraph, specify -2. |

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

