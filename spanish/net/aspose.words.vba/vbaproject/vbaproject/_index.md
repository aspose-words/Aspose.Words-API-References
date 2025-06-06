---
title: VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words para .NET
description: Crea un nuevo VbaProject fácilmente con nuestra herramienta de construcción. ¡Comienza tu aventura en la programación con un proyecto en blanco y da rienda suelta a tu creatividad!
type: docs
weight: 10
url: /es/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

Crea un espacio en blanco[`VbaProject`](../) .

```csharp
public VbaProject()
```

## Ejemplos

Muestra cómo crear un proyecto VBA usando macros.

```csharp
Document doc = new Document();

//Crea un nuevo proyecto VBA.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Crea un nuevo módulo y especifica un código fuente de macro.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

//Agrega el módulo al proyecto VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Ver también

* class [VbaProject](../)
* espacio de nombres [Aspose.Words.Vba](../../../aspose.words.vba/)
* asamblea [Aspose.Words](../../../)
