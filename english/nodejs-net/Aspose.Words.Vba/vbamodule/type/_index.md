---
title: VbaModule.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for NodeJs
description: "VbaModule.type property. Specifies whether the module is a procedural module, document module, class module, or designer module."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Vba/vbamodule/type/
---

## VbaModule.type property

Specifies whether the module is a procedural module, document module, class module, or designer module.


```js
get type(): Aspose.Words.Vba.VbaModuleType
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

