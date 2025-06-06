---
title: VbaModule.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar la propiedad VbaModule Name para administrar fácilmente los nombres de los módulos de su proyecto VBA para mejorar la organización y la eficiencia.
type: docs
weight: 20
url: /es/net/aspose.words.vba/vbamodule/name/
---
## VbaModule.Name property

Obtiene o establece el nombre del módulo del proyecto VBA.

```csharp
public string Name { get; set; }
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

Muestra cómo acceder a la información del proyecto VBA de un documento.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

//Un proyecto VBA contiene una colección de módulos VBA.
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules;

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Establezca el nuevo código fuente para el módulo VBA. Puede acceder a los módulos VBA de la colección por índice o por nombre.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

//Eliminar un módulo de la colección.
vbaModules.Remove(vbaModules[2]);
```

### Ver también

* class [VbaModule](../)
* espacio de nombres [Aspose.Words.Vba](../../../aspose.words.vba/)
* asamblea [Aspose.Words](../../../)
