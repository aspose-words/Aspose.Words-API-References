---
title: Range.replace method
linktitle: replace method
articleTitle: replace method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Range.replace method"
type: docs
weight: 90
url: /nodejs-net/aspose.words/range/replace/
---

## replace(pattern, replacement) {#string_string}

Replaces all occurrences of a specified character string pattern with a replacement string.


```js
replace(pattern: string, replacement: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | string | A string to be replaced. |
| replacement | string | A string to replace all occurrences of pattern. |

### Remarks

The pattern will not be used as regular expression.
Please use Aspose.Words.Range.Replace(System.Text.RegularExpressions.Regex,System.String) if you need regular expressions.

Used case-insensitive comparison.

Method is able to process breaks in both pattern and replacement strings.


You should use special meta-characters if you need to work with breaks:
* **&p** - paragraph break
  
* **&b** - section break
  
* **&m** - page break
  
* **&l** - manual line break
  

Use method[Range.replace()](./#string_string_findreplaceoptions) to have more flexible customization.



### Returns

The number of replacements made.


## replace(pattern, replacement, options) {#string_string_findreplaceoptions}

Replaces all occurrences of a specified character string pattern with a replacement string.


```js
replace(pattern: string, replacement: string, options: Aspose.Words.Replacing.FindReplaceOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern | string | A string to be replaced. |
| replacement | string | A string to replace all occurrences of pattern. |
| options | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### Remarks

The pattern will not be used as regular expression.
Please use Aspose.Words.Range.Replace(System.Text.RegularExpressions.Regex,System.String,Aspose.Words.Replacing.FindReplaceOptions) if you need regular expressions.

Method is able to process breaks in both pattern and replacement strings.


You should use special meta-characters if you need to work with breaks:
* **&p** - paragraph break
  
* **&b** - section break
  
* **&m** - page break
  
* **&l** - manual line break
  
* **&&** - & character
  



### Returns

The number of replacements made.


## Examples

Shows how to perform a find-and-replace text operation on the contents of a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Greetings, _FullName_!");

// Perform a find-and-replace operation on our document's contents and verify the number of replacements that took place.
let replacementCount = doc.range.replace("_FullName_", "John Doe");

expect(replacementCount).toEqual(1);
expect(doc.getText().trim()).toEqual("Greetings, John Doe!");
```

Shows how to add formatting to paragraphs in which a find-and-replace operation has found matches.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.writeln("This one will not!");
builder.write("This one also will.");

let paragraphs = doc.firstSection.body.paragraphs.toArray();

expect(paragraphs.at(0).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Left);
expect(paragraphs.at(1).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Left);
expect(paragraphs.at(2).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Left);

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
let options = new aw.Replacing.FindReplaceOptions();

// Set the "Alignment" property to "ParagraphAlignment.Right" to right-align every paragraph
// that contains a match that the find-and-replace operation finds.
options.applyParagraphFormat.alignment = aw.ParagraphAlignment.Right;

// Replace every full stop that is right before a paragraph break with an exclamation point.
var count = doc.range.replace(".&p", "!&p", options);

expect(count).toEqual(2);
paragraphs = doc.firstSection.body.paragraphs.toArray();
expect(paragraphs.at(0).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Right);
expect(paragraphs.at(1).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Left);
expect(paragraphs.at(2).paragraphFormat.alignment).toEqual(aw.ParagraphAlignment.Right);
expect(doc.getText().trim()).toEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                        "This one will not!\r" +
                        "This one also will!");
```

Shows how to replace all instances of String of text in a table and cell.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.write("Carrots");
builder.insertCell();
builder.write("50");
builder.endRow();
builder.insertCell();
builder.write("Potatoes");
builder.insertCell();
builder.write("50");
builder.endTable();

let options = new aw.Replacing.FindReplaceOptions();
options.matchCase = true;
options.findWholeWordsOnly = true;

// Perform a find-and-replace operation on an entire table.
table.range.replace("Carrots", "Eggs", options);

// Perform a find-and-replace operation on the last cell of the last row of the table.
table.lastRow.lastCell.range.replace("50", "20", options);

expect(table.getText().trim()).toEqual("Eggs\u000750\u0007\u0007" +
                        "Potatoes\u000720\u0007\u0007");
```

Shows how to toggle case sensitivity when performing a find-and-replace operation.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Ruby bought a ruby necklace.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
let options = new aw.Replacing.FindReplaceOptions();

// Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
// Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
options.matchCase = matchCase;

doc.range.replace("Ruby", "Jade", options);

expect(doc.getText().trim()).toEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.");
```

Shows how to toggle standalone word-only find-and-replace operations.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Jackson will meet you in Jacksonville.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
let options = new aw.Replacing.FindReplaceOptions();

// Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
// Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
options.findWholeWordsOnly = findWholeWordsOnly;

doc.range.replace("Jackson", "Louis", options);

expect(doc.getText().trim()).toEqual(
  findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville." );
```

Shows how to replace text in a document's footer.

```js
let doc = new aw.Document(base.myDir + "Footer.docx");

let headersFooters = doc.firstSection.headersFooters;
let footer = headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterPrimary);

let options = new aw.Replacing.FindReplaceOptions();
options.matchCase = false;
options.findWholeWordsOnly = false;

let currentYear = new Date().getYear();
footer.range.replace("(C) 2006 Aspose Pty Ltd.", `Copyright (C) ${currentYear} by Aspose Pty Ltd.`, options);

doc.save(base.artifactsDir + "HeaderFooter.ReplaceText.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [Range](../)

