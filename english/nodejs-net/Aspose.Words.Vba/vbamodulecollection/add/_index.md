---
title: VbaModuleCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Node.js
description: "VbaModuleCollection.add method. Adds a module to the collection."
type: docs
weight: 40
url: /nodejs-net/aspose.words.vba/vbamodulecollection/add/
---

## add(vbaModule) {#vbamodule}

Adds a module to the collection.


```js
add(vbaModule: Aspose.Words.Vba.VbaModule)
```

| Parameter | Type | Description |
| --- | --- | --- |
| vbaModule | [VbaModule](../../vbamodule/) |  |

### Examples

Shows how to create a VBA project using macros.

```js
let doc = new aw.Document();

// Create a new VBA project.
let project = new aw.Vba.VbaProject();
project.name = "Aspose.project";
doc.vbaProject = project;

// Create a new module and specify a macro source code.
let module = new aw.Vba.VbaModule();
module.name = "Aspose.Module";
module.type = aw.Vba.VbaModuleType.ProceduralModule;
module.sourceCode = "New source code";

// Add the module to the VBA project.
doc.vbaProject.modules.add(module);

doc.save(base.artifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### See Also

* module [Aspose.Words.Vba](../../)
* class [VbaModuleCollection](../)

