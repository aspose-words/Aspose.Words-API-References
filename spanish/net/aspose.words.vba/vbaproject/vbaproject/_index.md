---
title: VbaProject.VbaProject
second_title: Referencia de API de Aspose.Words para .NET
description: VbaProject constructor. Crea un VbaProject. en blanco
type: docs
weight: 10
url: /es/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

Crea un VbaProject. en blanco

```csharp
public VbaProject()
```

### Ejemplos

Muestra cómo crear un proyecto VBA usando macros.

```csharp
Document doc = new Document();

// Crea un nuevo proyecto VBA.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Crear un nuevo módulo y especificar un código fuente de macro.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Agregue el módulo al proyecto VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Ver también

* class [VbaProject](../)
* espacio de nombres [Aspose.Words.Vba](../../vbaproject/)
* asamblea [Aspose.Words](../../../)


