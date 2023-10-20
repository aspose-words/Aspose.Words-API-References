---
title: VbaProject Class
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words para .NET
description: Aspose.Words.Vba.VbaProject clase. Proporciona acceso a la información del proyecto VBA. Un proyecto VBA dentro del documento se define como una colección de módulos VBA en C#.
type: docs
weight: 6580
url: /es/net/aspose.words.vba/vbaproject/
---
## VbaProject class

Proporciona acceso a la información del proyecto VBA. Un proyecto VBA dentro del documento se define como una colección de módulos VBA.

Para obtener más información, visite el[Trabajar con macros VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) artículo de documentación.

```csharp
public class VbaProject
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [VbaProject](vbaproject/)() | Crea un espacio en blanco`VbaProject` . |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; set; } | Obtiene o establece la página de códigos del proyecto VBA. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Muestra si el`VbaProject` está firmado o no. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | Devuelve la colección de módulos del proyecto VBA. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | Obtiene o establece el nombre del proyecto VBA. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | Obtiene una colección de referencias de proyectos VBA. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | Realiza una copia del`VbaProject` . |

## Ejemplos

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

* espacio de nombres [Aspose.Words.Vba](../../aspose.words.vba/)
* asamblea [Aspose.Words](../../)
