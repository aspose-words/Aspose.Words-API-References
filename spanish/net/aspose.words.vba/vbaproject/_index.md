---
title: Class VbaProject
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Vba.VbaProject clase. Proporciona acceso a la información del proyecto VBA. Un proyecto VBA dentro del documento se define como una colección de módulos VBA.
type: docs
weight: 6270
url: /es/net/aspose.words.vba/vbaproject/
---
## VbaProject class

Proporciona acceso a la información del proyecto VBA. Un proyecto VBA dentro del documento se define como una colección de módulos VBA.

```csharp
public class VbaProject
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [VbaProject](vbaproject/)() | Crea un VbaProject. en blanco |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; } | Devuelve la página de códigos del proyecto VBA. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Muestra si el VbaProject está firmado o no. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | Devuelve la colección de módulos de proyecto de VBA. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | Obtiene o establece el nombre del proyecto VBA. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | Obtiene una colección de referencias de proyectos de VBA. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | Realiza una copia del`VbaProject` . |

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

* espacio de nombres [Aspose.Words.Vba](../../aspose.words.vba/)
* asamblea [Aspose.Words](../../)


