---
title: VbaModule Class
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words per .NET
description: Aspose.Words.Vba.VbaModule classe. Fornisce laccesso al modulo del progetto VBA in C#.
type: docs
weight: 6550
url: /it/net/aspose.words.vba/vbamodule/
---
## VbaModule class

Fornisce l'accesso al modulo del progetto VBA.

Per saperne di più, visita il[Lavorare con le macro VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) articolo di documentazione.

```csharp
public class VbaModule
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [VbaModule](vbamodule/)() | Crea un modulo vuoto. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Name](../../aspose.words.vba/vbamodule/name/) { get; set; } | Ottiene o imposta il nome del modulo del progetto VBA. |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode/) { get; set; } | Ottiene o imposta il codice sorgente del modulo di progetto VBA. |
| [Type](../../aspose.words.vba/vbamodule/type/) { get; set; } | Specifica se il modulo è un modulo procedurale, un modulo di documento, un modulo di classe o un modulo di progettazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone/)() | Esegue una copia del file`VbaModule` . |

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
