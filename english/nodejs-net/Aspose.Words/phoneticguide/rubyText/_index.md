---
title: PhoneticGuide.rubyText property
linktitle: rubyText property
articleTitle: rubyText property
second_title: Aspose.Words for NodeJs
description: "PhoneticGuide.rubyText property. Gets ruby text of the phonetic guide."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words/phoneticguide/rubyText/
---

## PhoneticGuide.rubyText property

Gets ruby text of the phonetic guide.


```js
get rubyText(): string
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
* class [PhoneticGuide](../)

