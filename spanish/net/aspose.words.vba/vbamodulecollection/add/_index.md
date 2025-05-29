---
title: VbaModuleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words para .NET
description: Mejore sin esfuerzo sus proyectos VBA con el método Add de VbaModuleCollection, que permite agregar módulos sin problemas para mejorar la funcionalidad.
type: docs
weight: 30
url: /es/net/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection.Add method

Agrega un módulo a la colección.

```csharp
public void Add(VbaModule vbaModule)
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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* espacio de nombres [Aspose.Words.Vba](../../../aspose.words.vba/)
* asamblea [Aspose.Words](../../../)
