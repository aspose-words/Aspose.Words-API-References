---
title: Document.VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words per .NET
description: Scopri come gestire efficacemente le proprietà di VbaProject. Impara a ottenere o impostare VbaProject per una maggiore automazione e flussi di lavoro semplificati.
type: docs
weight: 470
url: /it/net/aspose.words/document/vbaproject/
---
## Document.VbaProject property

Ottiene o imposta un`VbaProject` .

```csharp
public VbaProject VbaProject { get; set; }
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

* class [VbaProject](../../../aspose.words.vba/vbaproject/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
