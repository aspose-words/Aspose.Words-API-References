---
title: VbaModuleCollection.Item
second_title: Referencia de API de Aspose.Words para .NET
description: VbaModuleCollection propiedad. Recupera unVbaModule objeto por index.
type: docs
weight: 20
url: /es/net/aspose.words.vba/vbamodulecollection/item/
---
## VbaModuleCollection indexer (1 of 2)

Recupera un[`VbaModule`](../../vbamodule/) objeto por index.

```csharp
public VbaModule this[int index] { get; }
```

| Parámetro | Descripción |
| --- | --- |
| index | Índice de base cero del módulo a recuperar. |

### Ejemplos

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* espacio de nombres [Aspose.Words.Vba](../../vbamodulecollection/)
* asamblea [Aspose.Words](../../../)

---

## VbaModuleCollection indexer (2 of 2)

Recupera un[`VbaModule`](../../vbamodule/)objeto por nombre, o Nulo si no se encuentra.

```csharp
public VbaModule this[string name] { get; }
```

### Ejemplos

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* espacio de nombres [Aspose.Words.Vba](../../vbamodulecollection/)
* asamblea [Aspose.Words](../../../)


