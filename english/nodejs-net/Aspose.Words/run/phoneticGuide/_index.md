---
title: Run.phoneticGuide property
linktitle: phoneticGuide property
articleTitle: phoneticGuide property
second_title: Aspose.Words for NodeJs
description: "Run.phoneticGuide property. Gets a [Run.phoneticGuide](./) object."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/run/phoneticGuide/
---

## Run.phoneticGuide property

Gets a [Run.phoneticGuide](./) object.



```js
get phoneticGuide(): Aspose.Words.PhoneticGuide
```

### Examples

Shows how to get properties of the phonetic guide.

```js
let doc = new aw.Document(base.myDir + "Phonetic guide.docx");

let runs = doc.firstSection.body.firstParagraph.runs;
// Use phonetic guide in the Asian text.
expect(runs.at(0).isPhoneticGuide).toEqual(true);
expect(runs.at(0).phoneticGuide.baseText).toEqual("base");
expect(runs.at(0).phoneticGuide.rubyText).toEqual("ruby");
```

### See Also

* module [Aspose.Words](../../)
* class [Run](../)

