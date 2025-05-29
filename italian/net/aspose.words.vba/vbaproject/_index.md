---
title: VbaProject Class
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words per .NET
description: Sfrutta la potenza della classe Aspose.Words.Vba.VbaProject per gestire facilmente le informazioni e i moduli dei progetti VBA all'interno dei tuoi documenti. Migliora la tua automazione oggi stesso!
type: docs
weight: 7430
url: /it/net/aspose.words.vba/vbaproject/
---
## VbaProject class

Fornisce accesso alle informazioni del progetto VBA. Un progetto VBA all'interno del documento è definito come una raccolta di moduli VBA.

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
| [IsProtected](../../aspose.words.vba/vbaproject/isprotected/) { get; } | Mostra se il`VbaProject` è protetto da password. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Mostra se il`VbaProject` è firmato o no. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | Restituisce una raccolta di moduli di progetto VBA. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | Ottiene o imposta il nome del progetto VBA. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | Ottiene una raccolta di riferimenti al progetto VBA. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | Esegue una copia del`VbaProject` . |

## Esempi

Mostra come accedere alle informazioni del progetto VBA di un documento.

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
