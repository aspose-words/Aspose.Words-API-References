---
title: VbaModuleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi facilmente agli oggetti VbaModule con la proprietà Item di VbaModuleCollection. Migliora i tuoi progetti VBA con una facile indicizzazione e una gestione migliorata.
type: docs
weight: 20
url: /it/net/aspose.words.vba/vbamodulecollection/item/
---
## VbaModuleCollection indexer (1 of 2)

Recupera un[`VbaModule`](../../vbamodule/) oggetto per indice.

```csharp
public VbaModule this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Indice basato su zero del modulo da recuperare. |

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* spazio dei nomi [Aspose.Words.Vba](../../../aspose.words.vba/)
* assemblea [Aspose.Words](../../../)

---

## VbaModuleCollection indexer (2 of 2)

Recupera un[`VbaModule`](../../vbamodule/) oggetto per nome o Null se non trovato.

```csharp
public VbaModule this[string name] { get; }
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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* spazio dei nomi [Aspose.Words.Vba](../../../aspose.words.vba/)
* assemblea [Aspose.Words](../../../)
