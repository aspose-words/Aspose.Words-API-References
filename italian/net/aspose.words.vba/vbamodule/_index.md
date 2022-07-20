---
title: VbaModule
second_title: Aspose.Words per .NET API Reference
description: Fornisce laccesso al modulo del progetto VBA.
type: docs
weight: 6240
url: /it/net/aspose.words.vba/vbamodule/
---
## VbaModule class

Fornisce l'accesso al modulo del progetto VBA.

```csharp
public class VbaModule
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [VbaModule](vbamodule)() | Crea un modulo vuoto. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Name](../../aspose.words.vba/vbamodule/name) { get; set; } | Ottiene o imposta il nome del modulo del progetto VBA. |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode) { get; set; } | Ottiene o imposta il codice sorgente del modulo del progetto VBA. |
| [Type](../../aspose.words.vba/vbamodule/type) { get; set; } | Specifica se il modulo è un modulo procedurale, un modulo documento, un modulo di classe o un modulo designer. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone)() | Esegue una copia di[`VbaModule`](../vbamodule) . |

### Esempi

Mostra come accedere alle informazioni sul progetto VBA di un documento.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Un progetto VBA contiene una raccolta di moduli VBA.
VbaProject vbaProject = doc.VbaProject;
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Imposta un nuovo codice sorgente per il modulo VBA. Puoi accedere ai moduli VBA nella raccolta per indice o per nome.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Rimuove un modulo dalla raccolta.
vbaModules.Remove(vbaModules[2]);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Vba](../../aspose.words.vba)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->