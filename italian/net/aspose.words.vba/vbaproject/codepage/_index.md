---
title: VbaProject.CodePage
second_title: Aspose.Words per .NET API Reference
description: VbaProject proprietà. Restituisce la codepage del progetto VBA.
type: docs
weight: 20
url: /it/net/aspose.words.vba/vbaproject/codepage/
---
## VbaProject.CodePage property

Restituisce la codepage del progetto VBA.

```csharp
public int CodePage { get; }
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

* class [VbaProject](../)
* spazio dei nomi [Aspose.Words.Vba](../../vbaproject/)
* assemblea [Aspose.Words](../../../)


