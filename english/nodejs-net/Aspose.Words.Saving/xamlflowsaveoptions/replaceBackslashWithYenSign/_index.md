---
title: XamlFlowSaveOptions.replaceBackslashWithYenSign property
linktitle: replaceBackslashWithYenSign property
articleTitle: replaceBackslashWithYenSign property
second_title: Aspose.Words for Node.js
description: "XamlFlowSaveOptions.replaceBackslashWithYenSign property. Specifies whether backslash characters should be replaced with yen signs"
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/xamlflowsaveoptions/replaceBackslashWithYenSign/
---

## XamlFlowSaveOptions.replaceBackslashWithYenSign property

Specifies whether backslash characters should be replaced with yen signs.
Default value is ``false``.



```js
get replaceBackslashWithYenSign(): boolean
```

### Remarks

By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in
generated XAML documents. However, previous versions of Aspose.Words performed such replacements in certain
scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.


### Examples

Shows how to replace backslash characters with yen signs (Xaml).

```js
let doc = new aw.Document(base.myDir + "Korean backslash symbol.docx");

// By default, Aspose.words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in
// generated HTML documents. However, previous versions of Aspose.words performed such replacements in certain
// scenarios. This flag enables backward compatibility with previous versions of Aspose.words.
let saveOptions = new aw.Saving.XamlFlowSaveOptions();
saveOptions.replaceBackslashWithYenSign = true;

doc.save(base.artifactsDir + "HtmlSaveOptions.replaceBackslashWithYenSign.xaml", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [XamlFlowSaveOptions](../)

