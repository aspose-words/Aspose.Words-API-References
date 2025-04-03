---
title: TxtSaveOptions.maxCharactersPerLine property
linktitle: maxCharactersPerLine property
articleTitle: maxCharactersPerLine property
second_title: Aspose.Words for NodeJs
description: "TxtSaveOptions.maxCharactersPerLine property. Gets or sets an integer value that specifies the maximum number of characters per one line"
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/txtsaveoptions/maxCharactersPerLine/
---

## TxtSaveOptions.maxCharactersPerLine property

Gets or sets an integer value that specifies the maximum number of characters per one line.
The default value is 0, that means no limit.


```js
get maxCharactersPerLine(): number
```

### Examples

Shows how to set maximum number of characters per line.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
      "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Set 30 characters as maximum allowed per one line.
let saveOptions = new aw.Saving.TxtSaveOptions();
saveOptions.maxCharactersPerLine = 30;

doc.save(base.artifactsDir + "TxtSaveOptions.maxCharactersPerLine.txt", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [TxtSaveOptions](../)

