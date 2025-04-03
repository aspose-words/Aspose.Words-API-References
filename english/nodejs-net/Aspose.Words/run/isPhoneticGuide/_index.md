---
title: Run.isPhoneticGuide property
linktitle: isPhoneticGuide property
articleTitle: isPhoneticGuide property
second_title: Aspose.Words for NodeJs
description: "Run.isPhoneticGuide property. Gets a boolean value indicating either the run is a phonetic guide."
type: docs
weight: 20
url: /nodejs-net/aspose.words/run/isPhoneticGuide/
---

## Run.isPhoneticGuide property

Gets a boolean value indicating either the run is a phonetic guide.


```js
get isPhoneticGuide(): boolean
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

