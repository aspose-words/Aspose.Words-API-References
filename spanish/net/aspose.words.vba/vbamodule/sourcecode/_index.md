---
title: VbaModule.SourceCode
second_title: Referencia de API de Aspose.Words para .NET
description: VbaModule propiedad. Obtiene o establece el código fuente del módulo del proyecto VBA.
type: docs
weight: 30
url: /es/net/aspose.words.vba/vbamodule/sourcecode/
---
## VbaModule.SourceCode property

Obtiene o establece el código fuente del módulo del proyecto VBA.

```csharp
public string SourceCode { get; set; }
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

Muestra cómo acceder a la información del proyecto VBA de un documento.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Un proyecto VBA contiene una colección de módulos VBA.
VbaProject vbaProject = doc.VbaProject;
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Establecer nuevo código fuente para el módulo VBA. Puede acceder a los módulos de VBA en la colección por índice o por nombre.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Eliminar un módulo de la colección.
vbaModules.Remove(vbaModules[2]);
```

### Ver también

* class [VbaModule](../)
* espacio de nombres [Aspose.Words.Vba](../../vbamodule/)
* asamblea [Aspose.Words](../../../)


