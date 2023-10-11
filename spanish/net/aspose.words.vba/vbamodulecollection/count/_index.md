---
title: VbaModuleCollection.Count
second_title: Referencia de API de Aspose.Words para .NET
description: VbaModuleCollection propiedad. Devuelve el número de módulos VBA en la colección.
type: docs
weight: 10
url: /es/net/aspose.words.vba/vbamodulecollection/count/
---
## VbaModuleCollection.Count property

Devuelve el número de módulos VBA en la colección.

```csharp
public int Count { get; }
```

### Ejemplos

Muestra cómo acceder a la información del proyecto VBA de un documento.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Un proyecto VBA contiene una colección de módulos VBA.
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Establece un nuevo código fuente para el módulo VBA. Puede acceder a los módulos VBA de la colección por índice o por nombre.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Eliminar un módulo de la colección.
vbaModules.Remove(vbaModules[2]);
```

### Ver también

* class [VbaModuleCollection](../)
* espacio de nombres [Aspose.Words.Vba](../../vbamodulecollection/)
* asamblea [Aspose.Words](../../../)


