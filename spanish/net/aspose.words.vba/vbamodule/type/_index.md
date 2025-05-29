---
title: VbaModule.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Descubra la propiedad Tipo VbaModule, defina sus módulos como procedimentales, de documento, de clase o de diseñador para mejorar la funcionalidad y organización.
type: docs
weight: 40
url: /es/net/aspose.words.vba/vbamodule/type/
---
## VbaModule.Type property

Especifica si el módulo es un módulo de procedimiento, un módulo de documento, un módulo de clase o un módulo de diseñador.

```csharp
public VbaModuleType Type { get; set; }
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

* enum [VbaModuleType](../../vbamoduletype/)
* class [VbaModule](../)
* espacio de nombres [Aspose.Words.Vba](../../../aspose.words.vba/)
* asamblea [Aspose.Words](../../../)
