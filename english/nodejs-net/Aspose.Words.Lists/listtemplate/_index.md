---
title: ListTemplate enumeration
linktitle: ListTemplate enumeration
articleTitle: ListTemplate enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Lists.ListTemplate enumeration. Specifies one of the predefined list formats available in Microsoft Word."
type: docs
weight: 70
url: /nodejs-net/aspose.words.lists/listtemplate/
---

## ListTemplate enumeration

Specifies one of the predefined list formats available in Microsoft Word.

A list template value is used as a parameter into the
[ListCollection.add()](../listcollection/add/#listtemplate) method.

Aspose.Words list templates correspond to the 21 list templates available
in the Bullets and Numbering dialog box in Microsoft Word 2003.




### Members

| Name | Description |
| --- | --- |
| BulletDefault | Default bulleted list with 9 levels. Bullet of the first level is a disc, bullet of the second level is a circle, bullet of the third level is a square. Then formatting repeats for the remaining levels. |
| BulletDisk | Same as [ListTemplate.BulletDefault](./#BulletDefault). |
| BulletCircle | The bullet of the first level is a circle. The remaining levels are same as in [ListTemplate.BulletDefault](./#BulletDefault). |
| BulletSquare | The bullet of the first level is a square. The remaining levels are same as in [ListTemplate.BulletDefault](./#BulletDefault). |
| BulletDiamonds | The bullet of the first level is a 4-diamond Wingding character. The remaining levels are same as in [ListTemplate.BulletDefault](./#BulletDefault). |
| BulletArrowHead | The bullet of the first level is an arrow head Wingding character. The remaining levels are same as in [ListTemplate.BulletDefault](./#BulletDefault). |
| BulletTick | The bullet of the first level is a tick Wingding character. The remaining levels are same as in [ListTemplate.BulletDefault](./#BulletDefault). |
| NumberDefault | Default numbered list with 9 levels. Arabic numbering (1., 2., 3., ...) for the first level, lowercase letter numbering (a., b., c., ...) for the second level, lowercase roman numbering (i., ii., iii., ...) for the third level. Then formatting repeats for the remaining levels. |
| NumberArabicDot | Same as [ListTemplate.NumberDefault](./#NumberDefault). |
| NumberArabicParenthesis | The number of the first level is "1)". The remaining levels are same as in [ListTemplate.NumberDefault](./#NumberDefault). |
| NumberUppercaseRomanDot | The number of the first level is "I.". The remaining levels are same as in [ListTemplate.NumberDefault](./#NumberDefault). |
| NumberUppercaseLetterDot | The number of the first level is "A.". The remaining levels are same as in [ListTemplate.NumberDefault](./#NumberDefault). |
| NumberLowercaseLetterParenthesis | The number of the first level is "a)". The remaining levels are same as in [ListTemplate.NumberDefault](./#NumberDefault). |
| NumberLowercaseLetterDot | The number of the first level is "a.". The remaining levels are same as in [ListTemplate.NumberDefault](./#NumberDefault). |
| NumberLowercaseRomanDot | The number of the first level is "i.". The remaining levels are same as in [ListTemplate.NumberDefault](./#NumberDefault). |
| OutlineNumbers | An outline list with levels numbered "1), a), i), (1), (a), (i), 1., a., i.". |
| OutlineLegal | An outline list with levels are numbered "1., 1.1., 1.1.1, ...". |
| OutlineBullets | An outline lists with various bullets for different levels. |
| OutlineHeadingsArticleSection | An outline list with levels linked to Heading styles. |
| OutlineHeadingsLegal | An outline list with levels linked to Heading styles. |
| OutlineHeadingsNumbers | An outline list with levels linked to Heading styles. |
| OutlineHeadingsChapter | An outline list with levels linked to Heading styles. |

### Examples

Shows how to work with list levels.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

expect(builder.listFormat.isListItem).toEqual(false);

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Below are two types of lists that we can create using a document builder.
// 1 -  A numbered list:
// Numbered lists create a logical order for their paragraphs by numbering each item.
builder.listFormat.list = doc.lists.add(aw.Lists.ListTemplate.NumberDefault);

expect(builder.listFormat.isListItem).toEqual(true);

// By setting the "ListLevelNumber" property, we can increase the list level
// to begin a self-contained sub-list at the current list item.
// The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
// Deeper list levels use letters and lowercase Roman numerals. 
for (let i = 0; i < 9; i++)
{
  builder.listFormat.listLevelNumber = i;
  builder.writeln("Level " + i);
}

// 2 -  A bulleted list:
// This list will apply an indent and a bullet symbol ("•") before each paragraph.
// Deeper levels of this list will use different symbols, such as "■" and "○".
builder.listFormat.list = doc.lists.add(aw.Lists.ListTemplate.BulletDefault);

for (let i = 0; i < 9; i++)
{
  builder.listFormat.listLevelNumber = i;
  builder.writeln("Level " + i);
}

// We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
builder.listFormat.list = null;

expect(builder.listFormat.isListItem).toEqual(false);

doc.save(base.artifactsDir + "Lists.SpecifyListLevel.docx");
```

Shows how to restart numbering in a list by copying a list.

```js
let doc = new aw.Document();

// A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
// We can create nested lists by increasing the indent level. 
// We can begin and end a list by using a document builder's "ListFormat" property. 
// Each paragraph that we add between a list's start and the end will become an item in the list.
// Create a list from a Microsoft Word template, and customize its first list level.
let list1 = doc.lists.add(aw.Lists.ListTemplate.NumberArabicParenthesis);
list1.listLevels.at(0).font.color = "#FF0000";
list1.listLevels.at(0).alignment = aw.Lists.ListLevelAlignment.Right;

// Apply our list to some paragraphs.
let builder = new aw.DocumentBuilder(doc);

builder.writeln("List 1 starts below:");
builder.listFormat.list = list1;
builder.writeln("Item 1");
builder.writeln("Item 2");
builder.listFormat.removeNumbers();

// We can add a copy of an existing list to the document's list collection
// to create a similar list without making changes to the original.
let list2 = doc.lists.addCopy(list1);
list2.listLevels.at(0).font.color = "#0000FF";
list2.listLevels.at(0).startAt = 10;

// Apply the second list to new paragraphs.
builder.writeln("List 2 starts below:");
builder.listFormat.list = list2;
builder.writeln("Item 1");
builder.writeln("Item 2");
builder.listFormat.removeNumbers();

doc.save(base.artifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Shows how to create a document that contains all outline headings list templates.

```js
test('OutlineHeadingTemplates', () => {
  let doc = new aw.Document();
  let builder = new aw.DocumentBuilder(doc);

  let list = doc.lists.add(aw.Lists.ListTemplate.OutlineHeadingsArticleSection);
  addOutlineHeadingParagraphs(builder, list, "Aspose.words Outline - \"Article Section\"");

  list = doc.lists.add(aw.Lists.ListTemplate.OutlineHeadingsLegal);
  addOutlineHeadingParagraphs(builder, list, "Aspose.words Outline - \"Legal\"");

  builder.insertBreak(aw.BreakType.PageBreak);

  list = doc.lists.add(aw.Lists.ListTemplate.OutlineHeadingsNumbers);
  addOutlineHeadingParagraphs(builder, list, "Aspose.words Outline - \"Numbers\"");

  list = doc.lists.add(aw.Lists.ListTemplate.OutlineHeadingsChapter);
  addOutlineHeadingParagraphs(builder, list, "Aspose.words Outline - \"Chapters\"");

  doc.save(base.artifactsDir + "Lists.OutlineHeadingTemplates.docx");
});
```

### See Also

* module [Aspose.Words.Lists](../)

