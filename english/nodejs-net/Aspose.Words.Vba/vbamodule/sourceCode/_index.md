---
title: VbaModule.sourceCode property
linktitle: sourceCode property
articleTitle: sourceCode property
second_title: Aspose.Words for NodeJs
description: "VbaModule.sourceCode property. Gets or sets VBA project module source code."
type: docs
weight: 30
url: /nodejs-net/aspose.words.vba/vbamodule/sourceCode/
---

## VbaModule.sourceCode property

Gets or sets VBA project module source code.


```js
get sourceCode(): string
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

