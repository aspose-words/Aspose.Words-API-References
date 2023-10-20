---
title: VbaProject Class
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words per .NET
description: Aspose.Words.Vba.VbaProject classe. Fornisce laccesso alle informazioni sul progetto VBA. Un progetto VBA allinterno del documento è definito come una raccolta di moduli VBA in C#.
type: docs
weight: 6580
url: /it/net/aspose.words.vba/vbaproject/
---
## VbaProject class

Fornisce l'accesso alle informazioni sul progetto VBA. Un progetto VBA all'interno del documento è definito come una raccolta di moduli VBA.

Per saperne di più, visita il[Lavorare con le macro VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) articolo di documentazione.

```csharp
public class VbaProject
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [VbaProject](vbaproject/)() | Crea uno spazio vuoto`VbaProject` . |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; set; } | Ottiene o imposta la code page del progetto VBA. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Mostra se il`VbaProject` è firmato o no. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | Restituisce la raccolta di moduli di progetto VBA. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | Ottiene o imposta il nome del progetto VBA. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | Ottiene una raccolta di riferimenti al progetto VBA. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | Esegue una copia del file`VbaProject` . |

## Esempi

Mostra come accedere alle informazioni sul progetto VBA di un documento.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Un progetto VBA contiene una raccolta di moduli VBA.
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Imposta il nuovo codice sorgente per il modulo VBA. È possibile accedere ai moduli VBA nella raccolta tramite indice o nome.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Rimuove un modulo dalla raccolta.
vbaModules.Remove(vbaModules[2]);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Vba](../../aspose.words.vba/)
* assemblea [Aspose.Words](../../)
