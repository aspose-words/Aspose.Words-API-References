---
title: VbaProject.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Node.js
description: "VbaProject.name property. Gets or sets VBA project name."
type: docs
weight: 60
url: /nodejs-net/aspose.words.vba/vbaproject/name/
---

## VbaProject.name property

Gets or sets VBA project name.


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
* class [VbaProject](../)

