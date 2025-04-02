---
title: VbaModule.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for NodeJs
description: "VbaModule.name property. Gets or sets VBA project module name."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Vba/vbamodule/name/
---

## VbaModule.name property

Gets or sets VBA project module name.


```js
get name(): string
```

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
* class [VbaModule](../)

