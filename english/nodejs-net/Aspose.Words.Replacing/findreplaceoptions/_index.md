---
title: FindReplaceOptions class
linktitle: FindReplaceOptions class
articleTitle: FindReplaceOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Replacing.FindReplaceOptions class. Specifies options for find/replace operations"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Replacing/findreplaceoptions/
---

## FindReplaceOptions class

Specifies options for find/replace operations.
To learn more, visit the [Find and Replace](https://docs.aspose.com/words/nodejs-net/find-and-replace/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [FindReplaceOptions()](./constructor/#default) | Initializes a new instance of the FindReplaceOptions class with default settings. |
| [FindReplaceOptions(direction)](./constructor/#findreplacedirection) | Initializes a new instance of the FindReplaceOptions class with the specified direction. |
| [FindReplaceOptions(replacingCallback)](./constructor/#ireplacingcallback) | Initializes a new instance of the FindReplaceOptions class with the specified replacing callback. |
| [FindReplaceOptions(direction, replacingCallback)](./constructor/#findreplacedirection_ireplacingcallback) | Initializes a new instance of the FindReplaceOptions class with the specified direction and replacing callback. |

### Properties

| Name | Description |
| --- | --- |
| [applyFont](./applyFont/) | Text formatting applied to new content. |
| [applyParagraphFormat](./applyParagraphFormat/) | Paragraph formatting applied to new content. |
| [direction](./direction/) | Selects direction for replace. Default value is [FindReplaceDirection.Forward](../findreplacedirection/#Forward). |
| [findWholeWordsOnly](./findWholeWordsOnly/) | True indicates the oldValue must be a standalone word. |
| [ignoreDeleted](./ignoreDeleted/) | Gets or sets a boolean value indicating either to ignore text inside delete revisions. The default value is ``False``. |
| [ignoreFieldCodes](./ignoreFieldCodes/) | Gets or sets a boolean value indicating either to ignore text inside field codes. The default value is ``False``. |
| [ignoreFields](./ignoreFields/) | Gets or sets a boolean value indicating either to ignore text inside fields. The default value is ``False``. |
| [ignoreFootnotes](./ignoreFootnotes/) | Gets or sets a boolean value indicating either to ignore footnotes. The default value is ``False``. |
| [ignoreInserted](./ignoreInserted/) | Gets or sets a boolean value indicating either to ignore text inside insert revisions. The default value is ``False``. |
| [ignoreShapes](./ignoreShapes/) | Gets or sets a boolean value indicating either to ignore shapes within a text. |
| [ignoreStructuredDocumentTags](./ignoreStructuredDocumentTags/) | Gets or sets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../Aspose.Words.Markup/structureddocumenttag/). The default value is ``False``. |
| [legacyMode](./legacyMode/) | Gets or sets a boolean value indicating that old find/replace algorithm is used. |
| [matchCase](./matchCase/) | True indicates case-sensitive comparison, false indicates case-insensitive comparison. |
| [replacementFormat](./replacementFormat/) | Specifies format of the replacement. Default is [ReplacementFormat.Text](../replacementformat/#Text). |
| [replacingCallback](./replacingCallback/) | The user-defined method which is called before every replace occurrence. |
| [smartParagraphBreakReplacement](./smartParagraphBreakReplacement/) | Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph. |
| [useLegacyOrder](./useLegacyOrder/) | True indicates that a text search is performed sequentially from top to bottom considering the text boxes. Default value is ``False``. |
| [useSubstitutions](./useSubstitutions/) | Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns. The default value is ``False``. |

### Examples

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

### See Also

* module [Aspose.Words.Replacing](../)

