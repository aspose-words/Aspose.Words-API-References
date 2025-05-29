---
title: VbaProject.IsSigned
linktitle: IsSigned
articleTitle: IsSigned
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsSigned di VbaProject per verificare facilmente le firme dei progetti e migliorare la sicurezza del codice. Assicurati che i tuoi progetti VBA siano affidabili!
type: docs
weight: 40
url: /it/net/aspose.words.vba/vbaproject/issigned/
---
## VbaProject.IsSigned property

Mostra se il[`VbaProject`](../) è firmato o no.

```csharp
public bool IsSigned { get; }
```

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

* class [VbaProject](../)
* spazio dei nomi [Aspose.Words.Vba](../../../aspose.words.vba/)
* assemblea [Aspose.Words](../../../)
