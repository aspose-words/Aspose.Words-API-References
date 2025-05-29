---
title: VbaProject.IsSigned
linktitle: IsSigned
articleTitle: IsSigned
second_title: Aspose.Words para .NET
description: Descubra la propiedad IsSigned de VbaProject para verificar fácilmente las firmas de proyectos y mejorar la seguridad de su código. ¡Asegure la confianza de sus proyectos VBA!
type: docs
weight: 40
url: /es/net/aspose.words.vba/vbaproject/issigned/
---
## VbaProject.IsSigned property

Muestra si el[`VbaProject`](../) está firmado o no.

```csharp
public bool IsSigned { get; }
```

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

* class [VbaProject](../)
* espacio de nombres [Aspose.Words.Vba](../../../aspose.words.vba/)
* asamblea [Aspose.Words](../../../)
