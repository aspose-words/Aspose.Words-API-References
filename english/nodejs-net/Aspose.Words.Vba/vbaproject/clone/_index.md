---
title: VbaProject.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for NodeJs
description: "VbaProject.clone method. Performs a copy of the [VbaProject](../)."
type: docs
weight: 80
url: /nodejs-net/Aspose.Words.Vba/vbaproject/clone/
---

## clone() {#default}

Performs a copy of the [VbaProject](../).



```js
clone()
```

### Returns

The cloned [VbaProject](../).


### Examples

Shows how to deep clone a VBA project and module.

```js
let doc = new aw.Document(base.myDir + "VBA project.docm");
let destDoc = new aw.Document();

let copyVbaProject = doc.vbaProject.clone();
destDoc.vbaProject = copyVbaProject;

// In the destination document, we already have a module named "Module1"
// because we cloned it along with the project. We will need to remove the module.
let oldVbaModule = destDoc.vbaProject.modules.at("Module1");
let copyVbaModule = doc.vbaProject.modules.at("Module1").clone();
destDoc.vbaProject.modules.remove(oldVbaModule);
destDoc.vbaProject.modules.add(copyVbaModule);

destDoc.save(base.artifactsDir + "VbaProject.CloneVbaProject.docm");
```

### See Also

* module [Aspose.Words.Vba](../../)
* class [VbaProject](../)

