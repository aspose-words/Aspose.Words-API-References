---
title: Style class
linktitle: Style class
articleTitle: Style class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Style class. Represents a single built-in or user-defined style"
type: docs
weight: 1250
url: /nodejs-net/aspose.words/style/
---

## Style class

Represents a single built-in or user-defined style.
To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/nodejs-net/working-with-styles-and-themes/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [aliases](./aliases/) | Gets all aliases of this style. If style has no aliases then empty array of string is returned. |
| [automaticallyUpdate](./automaticallyUpdate/) | Specifies whether this style is automatically redefined based on the appropriate value. |
| [baseStyleName](./baseStyleName/) | Gets/sets the name of the style this style is based on. |
| [builtIn](./builtIn/) | True if this style is one of the built-in styles in MS Word. |
| [document](./document/) | Gets the owner document. |
| [font](./font/) | Gets the character formatting of the style. |
| [isHeading](./isHeading/) | True when the style is one of the built-in Heading styles. |
| [isQuickStyle](./isQuickStyle/) | Specifies whether this style is shown in the Quick Style gallery inside MS Word UI. |
| [linkedStyleName](./linkedStyleName/) | Gets/sets the name of the [Style](./) linked to this one. Returns empty string if no styles are linked. |
| [list](./list/) | Gets the list that defines formatting of this list style. |
| [listFormat](./listFormat/) | Provides access to the list formatting properties of a paragraph style. |
| [locked](./locked/) | Specifies whether this style is locked. |
| [name](./name/) | Gets or sets the name of the style. |
| [nextParagraphStyleName](./nextParagraphStyleName/) | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. |
| [paragraphFormat](./paragraphFormat/) | Gets the paragraph formatting of the style. |
| [priority](./priority/) | Gets/sets the integer value that represents the priority for sorting the styles in the Styles task pane. |
| [semiHidden](./semiHidden/) | Gets/sets whether the style hides from the Styles gallery and from the Styles task pane. |
| [styleIdentifier](./styleIdentifier/) | Gets the locale independent style identifier for a built-in style. |
| [styles](./styles/) | Gets the collection of styles this style belongs to. |
| [type](./type/) | Gets the style type (paragraph or character). |
| [unhideWhenUsed](./unhideWhenUsed/) | Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane. True when the used style should be shown in the Styles gallery. |

### Methods

| Name | Description |
| --- | --- |
|[ asTableStyle()](./asTableStyle/#default) |  |
|[ equals(style)](./equals/#style) | Compares with the specified style. Styles Istds are compared for built-in styles only. Styles defaults are not included in comparison. Base style, linked style and next paragraph style are recursively compared. |
|[ remove()](./remove/#default) | Removes the specified style from the document. |

### Examples

Shows how to create and apply a custom style.

```js
let doc = new aw.Document();

let style = doc.styles.add(aw.StyleType.Paragraph, "MyStyle");
style.font.name = "Times New Roman";
style.font.size = 16;
style.font.color = "#000080";
// Automatically redefine style.
style.automaticallyUpdate = true;

let builder = new aw.DocumentBuilder(doc);

// Apply one of the styles from the document to the paragraph that the document builder is creating.
builder.paragraphFormat.style = doc.styles.at("MyStyle");
builder.writeln("Hello world!");

let firstParagraphStyle = doc.firstSection.body.firstParagraph.paragraphFormat.style;

expect(firstParagraphStyle).toEqual(style);

// Remove our custom style from the document's styles collection.
doc.styles.at("MyStyle").remove();

firstParagraphStyle = doc.firstSection.body.firstParagraph.paragraphFormat.style;

// Any text that used a removed style reverts to the default formatting.
expect([...doc.styles].every(s => s.name == "MyStyle")).toEqual(false);
expect(firstParagraphStyle.font.name).toEqual("Times New Roman");
expect(firstParagraphStyle.font.size).toEqual(12.0);
expect(firstParagraphStyle.font.color).toEqual(base.emptyColor);
```

Shows how to create and use a paragraph style with list formatting.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a custom paragraph style.
let style = doc.styles.add(aw.StyleType.Paragraph, "MyStyle1");
style.font.size = 24;
style.font.name = "Verdana";
style.paragraphFormat.spaceAfter = 12;

// Create a list and make sure the paragraphs that use this style will use this list.
style.listFormat.list = doc.lists.add(aw.Lists.ListTemplate.BulletDefault);
style.listFormat.listLevelNumber = 0;

// Apply the paragraph style to the document builder's current paragraph, and then add some text.
builder.paragraphFormat.style = style;
builder.writeln("Hello World: MyStyle1, bulleted list.");

// Change the document builder's style to one that has no list formatting and write another paragraph.
builder.paragraphFormat.style = doc.styles.at("Normal");
builder.writeln("Hello World: Normal.");

builder.document.save(base.artifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### See Also

* module [Aspose.Words](../)

