---
title: Style.aliases property
linktitle: aliases property
articleTitle: aliases property
second_title: Aspose.Words for NodeJs
description: "Style.aliases property. Gets all aliases of this style"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/style/aliases/
---

## Style.aliases property

Gets all aliases of this style. If style has no aliases then empty array of string is returned.


```js
get aliases(): string[]
```

### Examples

Shows how to use style aliases.

```js
let doc = new aw.Document(base.myDir + "Style with alias.docx");

// This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// If a style's name has multiple values separated by commas, each clause is a separate alias.
let style = doc.styles.at("MyStyle");
expect(style.aliases).toEqual(["MyStyle Alias 1", "MyStyle Alias 2"]);
expect(style.baseStyleName).toEqual("Title");
expect(style.linkedStyleName).toEqual("MyStyle Char");

// We can reference a style using its alias, as well as its name.
expect(doc.styles.at("MyStyle Alias 2")).toEqual(doc.styles.at("MyStyle Alias 1"));

let builder = new aw.DocumentBuilder(doc);
builder.moveToDocumentEnd();
builder.paragraphFormat.style = doc.styles.at("MyStyle Alias 1");
builder.writeln("Hello world!");
builder.paragraphFormat.style = doc.styles.at("MyStyle Alias 2");
builder.write("Hello again!");

expect(doc.firstSection.body.paragraphs.at(1).paragraphFormat.style).toEqual(doc.firstSection.body.paragraphs.at(0).paragraphFormat.style);
```

### See Also

* module [Aspose.Words](../../)
* class [Style](../)

