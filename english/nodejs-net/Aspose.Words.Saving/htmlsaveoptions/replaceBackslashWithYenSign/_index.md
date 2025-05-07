---
title: HtmlSaveOptions.replaceBackslashWithYenSign property
linktitle: replaceBackslashWithYenSign property
articleTitle: replaceBackslashWithYenSign property
second_title: Aspose.Words for Node.js
description: "HtmlSaveOptions.replaceBackslashWithYenSign property. Specifies whether backslash characters should be replaced with yen signs"
type: docs
weight: 420
url: /nodejs-net/aspose.words.saving/htmlsaveoptions/replaceBackslashWithYenSign/
---

## HtmlSaveOptions.replaceBackslashWithYenSign property

Specifies whether backslash characters should be replaced with yen signs.
Default value is ``false``.



```js
get replaceBackslashWithYenSign(): boolean
```

### Remarks

By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in
generated HTML documents. However, previous versions of Aspose.Words performed such replacements in certain
scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.


### Examples

Shows how to replace backslash characters with yen signs (Html).

```js
let doc = new aw.Document(base.myDir + "Korean backslash symbol.docx");

// By default, Aspose.words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in
// generated HTML documents. However, previous versions of Aspose.words performed such replacements in certain
// scenarios. This flag enables backward compatibility with previous versions of Aspose.words.
let saveOptions = new aw.Saving.HtmlSaveOptions();
saveOptions.replaceBackslashWithYenSign = true;

doc.save(base.artifactsDir + "HtmlSaveOptions.replaceBackslashWithYenSign.html", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

