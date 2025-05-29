---
title: VbaModuleType Enum
linktitle: VbaModuleType
articleTitle: VbaModuleType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Vba.VbaModuleType, que define tipos de modelos en proyectos VBA para una mejor automatización y una gestión optimizada de documentos.
type: docs
weight: 7420
url: /es/net/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enumeration

Especifica el tipo de un modelo en un proyecto VBA.

```csharp
public enum VbaModuleType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| DocumentModule | `0` | Un tipo de elemento de proyecto de VBA que especifica un módulo para macros integradas y operaciones de acceso programático que están asociadas con un documento. |
| ProceduralModule | `1` | Una colección de subrutinas y funciones. |
| ClassModule | `2` | Un módulo que contiene la definición de un nuevo objeto. Cada instancia de una clase crea un nuevo objeto, y los procedimientos definidos en el módulo se convierten en propiedades y métodos del objeto. |
| DesignerModule | `3` | Un módulo VBA que extiende los métodos y propiedades de un control ActiveX que se ha registrado con el proyecto. |

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

* espacio de nombres [Aspose.Words.Vba](../../aspose.words.vba/)
* asamblea [Aspose.Words](../../)
