---
title: Font.localeId property
linktitle: localeId property
articleTitle: localeId property
second_title: Aspose.Words for NodeJs
description: "Font.localeId property. Gets or sets the locale identifier (language) of the formatted characters."
type: docs
weight: 200
url: /nodejs-net/Aspose.Words/font/localeId/
---

## Font.localeId property

Gets or sets the locale identifier (language) of the formatted characters.


```js
get localeId(): number
```

### Remarks

For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx


### Examples

Shows how to set the locale of the text that we are adding with a document builder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// If we set the font's locale to English and insert some Russian text,
// the English locale spell checker will not recognize the text and detect it as a spelling error.
builder.font.localeId = new CultureInfo("en-US", false).LCID;
builder.writeln("Привет!");

// Set a matching locale for the text that we are about to add to apply the appropriate spell checker.
builder.font.localeId = new CultureInfo("ru-RU", false).LCID;
builder.writeln("Привет!");

doc.save(base.artifactsDir + "Font.localeId.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Font](../)

