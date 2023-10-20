---
title: VbaModule
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words para .NET
description: VbaModule constructor. Crea un módulo vacío en C#.
type: docs
weight: 10
url: /es/net/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule constructor

Crea un módulo vacío.

```csharp
public VbaModule()
```

## Ejemplos

Muestra cómo crear un proyecto VBA usando macros.

```csharp
Document doc = new Document();

// Crea un nuevo proyecto VBA.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Crea un nuevo módulo y especifica un código fuente de macro.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Agrega el módulo al proyecto VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Ver también

* class [VbaModule](../)
* espacio de nombres [Aspose.Words.Vba](../../../aspose.words.vba/)
* asamblea [Aspose.Words](../../../)
