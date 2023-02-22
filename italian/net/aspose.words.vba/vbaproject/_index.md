---
title: Class VbaProject
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Vba.VbaProject classe. Fornisce laccesso alle informazioni sul progetto VBA. Un progetto VBA allinterno del documento è definito come una raccolta di moduli VBA.
type: docs
weight: 6270
url: /it/net/aspose.words.vba/vbaproject/
---
## VbaProject class

Fornisce l'accesso alle informazioni sul progetto VBA. Un progetto VBA all'interno del documento è definito come una raccolta di moduli VBA.

```csharp
public class VbaProject
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [VbaProject](vbaproject/)() | Crea un VbaProject vuoto. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; } | Restituisce la codepage del progetto VBA. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Mostra se il VbaProject è firmato o meno. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | Restituisce la raccolta dei moduli del progetto VBA. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | Ottiene o imposta il nome del progetto VBA. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | Ottiene una raccolta di riferimenti al progetto VBA. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | Esegue una copia di`VbaProject` . |

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

* spazio dei nomi [Aspose.Words.Vba](../../aspose.words.vba/)
* assemblea [Aspose.Words](../../)


