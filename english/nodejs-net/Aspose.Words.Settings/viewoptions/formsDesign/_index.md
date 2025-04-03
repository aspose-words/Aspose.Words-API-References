---
title: ViewOptions.formsDesign property
linktitle: formsDesign property
articleTitle: formsDesign property
second_title: Aspose.Words for NodeJs
description: "ViewOptions.formsDesign property. Specifies whether the document is in forms design mode."
type: docs
weight: 30
url: /nodejs-net/aspose.words.settings/viewoptions/formsDesign/
---

## ViewOptions.formsDesign property

Specifies whether the document is in forms design mode.


```js
get formsDesign(): boolean
```

### Remarks

Currently works only for documents in WordML format.




### Examples

Shows how to enable/disable forms design mode.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

// Set the "FormsDesign" property to "false" to keep forms design mode disabled.
// Set the "FormsDesign" property to "true" to enable forms design mode.
doc.viewOptions.formsDesign = useFormsDesign;

doc.save(base.artifactsDir + "ViewOptions.formsDesign.xml");

expect(fs.readFileSync(base.artifactsDir + "ViewOptions.formsDesign.xml").toString().includes("<w:formsDesign />")).toEqual(useFormsDesign);
```

### See Also

* module [Aspose.Words.Settings](../../)
* class [ViewOptions](../)

