---
title: Document.removeMacros method
linktitle: removeMacros method
articleTitle: removeMacros method
second_title: Aspose.Words for Node.js
description: "Document.removeMacros method. Removes all macros (the VBA project) as well as toolbars and command customizations from the document."
type: docs
weight: 690
url: /nodejs-net/aspose.words/document/removeMacros/
---

## removeMacros() {#default}

Removes all macros (the VBA project) as well as toolbars and command customizations from the document.


```js
removeMacros()
```

### Remarks

By removing all macros from a document you can ensure the document contains no macro viruses.




### Examples

Shows how to remove all macros from a document.

```js
let doc = new aw.Document(base.myDir + "Macro.docm");
expect(doc.hasMacros).toEqual(true);
expect(doc.vbaProject.name).toEqual("Project");
// Remove the document's VBA project, along with all its macros.
doc.removeMacros();
expect(doc.hasMacros).toEqual(false);
expect(doc.vbaProject).toEqual(null);
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

