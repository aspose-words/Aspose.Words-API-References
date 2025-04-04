---
title: CleanupOptions class
linktitle: CleanupOptions class
articleTitle: CleanupOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.CleanupOptions class. Allows to specify options for document cleaning"
type: docs
weight: 170
url: /nodejs-net/aspose.words/cleanupoptions/
---

## CleanupOptions class

Allows to specify options for document cleaning.
To learn more, visit the [Clean Up a Document](https://docs.aspose.com/words/nodejs-net/clean-up-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [CleanupOptions()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [duplicateStyle](./duplicateStyle/) | Gets/sets a flag indicating whether duplicate styles should be removed from document. Default value is ``false``. |
| [unusedBuiltinStyles](./unusedBuiltinStyles/) | Specifies that unused [Style.builtIn](../style/builtIn/) styles should be removed from document. |
| [unusedLists](./unusedLists/) | Specifies whether unused list and list definitions should be removed from document. Default value is ``true``. |
| [unusedStyles](./unusedStyles/) | Specifies whether unused styles should be removed from document. Default value is ``true``. |

### Examples

Shows how to remove all unused custom styles from a document.

```js
let doc = new aw.Document();

doc.styles.add(aw.StyleType.List, "MyListStyle1");
doc.styles.add(aw.StyleType.List, "MyListStyle2");
doc.styles.add(aw.StyleType.Character, "MyParagraphStyle1");
doc.styles.add(aw.StyleType.Character, "MyParagraphStyle2");

// Combined with the built-in styles, the document now has eight styles.
// A custom style is marked as "used" while there is any text within the document
// formatted in that style. This means that the 4 styles we added are currently unused.
expect(doc.styles.count).toEqual(8);

// Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
let builder = new aw.DocumentBuilder(doc);
builder.font.style = doc.styles.at("MyParagraphStyle1");
builder.writeln("Hello world!");

let list = doc.lists.add(doc.styles.at("MyListStyle1"));
builder.listFormat.list = list;
builder.writeln("Item 1");
builder.writeln("Item 2");

// Now, there is one unused character style and one unused list style.
// The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
let cleanupOptions = new aw.CleanupOptions();
cleanupOptions.unusedLists = true;
cleanupOptions.unusedStyles = true;
cleanupOptions.unusedBuiltinStyles = true;

doc.cleanup(cleanupOptions);

expect(doc.styles.count).toEqual(4);

// Removing every node that a custom style is applied to marks it as "unused" again. 
// Rerun the Cleanup method to remove them.
doc.firstSection.body.removeAllChildren();
doc.cleanup(cleanupOptions);

expect(doc.styles.count).toEqual(2);
```

### See Also

* module [Aspose.Words](../)

