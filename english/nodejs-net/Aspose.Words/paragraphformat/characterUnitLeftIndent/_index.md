---
title: ParagraphFormat.characterUnitLeftIndent property
linktitle: characterUnitLeftIndent property
articleTitle: characterUnitLeftIndent property
second_title: Aspose.Words for NodeJs
description: "ParagraphFormat.characterUnitLeftIndent property. Gets or sets the left indent value (in characters) for the specified paragraphs."
type: docs
weight: 80
url: /nodejs-net/aspose.words/paragraphformat/characterUnitLeftIndent/
---

## ParagraphFormat.characterUnitLeftIndent property

Gets or sets the left indent value (in characters) for the specified paragraphs.


```js
get characterUnitLeftIndent(): number
```

### Examples

Shows how to change paragraph spacing and indents.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
let format = doc.firstSection.body.firstParagraph.paragraphFormat;

// Below are five different spacing options, along with the properties that their configuration indirectly affects.
// 1 -  Left indent:
expect(0.0).toEqual(format.leftIndent);

format.characterUnitLeftIndent = 10.0;

expect(120.0).toEqual(format.leftIndent);

// 2 -  Right indent:
expect(0.0).toEqual(format.rightIndent);

format.characterUnitRightIndent = -5.5;

expect(-66.0).toEqual(format.rightIndent);

// 3 -  Hanging indent:
expect(0.0).toEqual(format.firstLineIndent);

format.characterUnitFirstLineIndent = 20.3;

expect(format.firstLineIndent).toBeCloseTo(243.59, 1);

// 4 -  Line spacing before paragraphs:
expect(0.0).toEqual(format.spaceBefore);

format.lineUnitBefore = 5.1;

expect(format.spaceBefore).toBeCloseTo(61.1, 1);

// 5 -  Line spacing after paragraphs:
expect(0.0).toEqual(format.spaceAfter);

format.lineUnitAfter = 10.9;

expect(format.spaceAfter).toBeCloseTo(130.8, 1);

builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.write("测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试" +
  "文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

