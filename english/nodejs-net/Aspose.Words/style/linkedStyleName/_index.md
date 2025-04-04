---
title: Style.linkedStyleName property
linktitle: linkedStyleName property
articleTitle: linkedStyleName property
second_title: Aspose.Words for Node.js
description: "Style.linkedStyleName property. Gets/sets the name of the [Style](../) linked to this one"
type: docs
weight: 90
url: /nodejs-net/aspose.words/style/linkedStyleName/
---

## Style.linkedStyleName property

Gets/sets the name of the [Style](../) linked to this one. Returns empty string if no styles are linked.



```js
get linkedStyleName(): string
```

### Remarks

It is only allowed to link the paragraph style to the character style and vice versa.

Setting LinkedStyleName for the current style automatically leads to setting LinkedStyleName for the linked style.

Assigning the empty string is equivalent to unlinking the previously linked style.




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

Shows how to link styles among themselves.

```js
let doc = new aw.Document();

let styleHeading1 = doc.styles.at(aw.StyleIdentifier.Heading1);

let styleHeading1Char = doc.styles.add(aw.StyleType.Character, "Heading 1 Char");
styleHeading1Char.font.name = "Verdana";
styleHeading1Char.font.bold = true;
styleHeading1Char.font.border.lineStyle = aw.LineStyle.Dot;
styleHeading1Char.font.border.lineWidth = 15;

styleHeading1.linkedStyleName = "Heading 1 Char";

expect(styleHeading1.linkedStyleName).toEqual("Heading 1 Char");
expect(styleHeading1Char.linkedStyleName).toEqual("Heading 1");
```

### See Also

* module [Aspose.Words](../../)
* class [Style](../)

