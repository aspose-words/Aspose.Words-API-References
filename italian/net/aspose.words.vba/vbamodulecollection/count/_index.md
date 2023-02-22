---
title: VbaModuleCollection.Count
second_title: Aspose.Words per .NET API Reference
description: VbaModuleCollection proprietà. Restituisce il numero di moduli VBA nella raccolta.
type: docs
weight: 10
url: /it/net/aspose.words.vba/vbamodulecollection/count/
---
## VbaModuleCollection.Count property

Restituisce il numero di moduli VBA nella raccolta.

```csharp
public int Count { get; }
```

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

* class [VbaModuleCollection](../)
* spazio dei nomi [Aspose.Words.Vba](../../vbamodulecollection/)
* assemblea [Aspose.Words](../../../)


