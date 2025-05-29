---
title: VbaModuleCollection Class
linktitle: VbaModuleCollection
articleTitle: VbaModuleCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Vba.VbaModuleCollection, su herramienta esencial para administrar objetos VbaModule de manera eficiente en la automatización de documentos.
type: docs
weight: 7410
url: /es/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

Representa una colección de[`VbaModule`](../vbamodule/) objetos.

Para obtener más información, visite el[Trabajar con macros de VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) Artículo de documentación.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | Devuelve el número de módulos VBA en la colección. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | Recupera una[`VbaModule`](../vbamodule/) objeto por índice. (2 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(*[VbaModule](../vbamodule/)*) | Agrega un módulo a la colección. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(*[VbaModule](../vbamodule/)*) | Elimina el módulo especificado de la colección. |

## Ejemplos

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

* class [VbaModule](../vbamodule/)
* espacio de nombres [Aspose.Words.Vba](../../aspose.words.vba/)
* asamblea [Aspose.Words](../../)
