---
title: Class VbaModuleCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Vba.VbaModuleCollection clase. Representa una colección deVbaModule objetos.
type: docs
weight: 6560
url: /es/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

Representa una colección de[`VbaModule`](../vbamodule/) objetos.

Para obtener más información, visite el[Trabajar con macros VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) artículo de documentación.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | Devuelve el número de módulos VBA en la colección. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | Recupera un[`VbaModule`](../vbamodule/) objeto por index. (2 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(VbaModule) | Agrega un módulo a la colección. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(VbaModule) | Elimina el módulo especificado de la colección. |

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

* class [VbaModule](../vbamodule/)
* espacio de nombres [Aspose.Words.Vba](../../aspose.words.vba/)
* asamblea [Aspose.Words](../../)


