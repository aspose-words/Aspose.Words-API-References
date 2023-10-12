---
title: Class VbaModuleCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Vba.VbaModuleCollection classe. Rappresenta una raccolta diVbaModule oggetti.
type: docs
weight: 6560
url: /it/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

Rappresenta una raccolta di[`VbaModule`](../vbamodule/) oggetti.

Per saperne di più, visita il[Lavorare con le macro VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) articolo di documentazione.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | Restituisce il numero di moduli VBA nella raccolta. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | Recupera a[`VbaModule`](../vbamodule/) oggetto per indice. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(VbaModule) | Aggiunge un modulo alla raccolta. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(VbaModule) | Rimuove il modulo specificato dalla raccolta. |

### Esempi

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

* class [VbaModule](../vbamodule/)
* spazio dei nomi [Aspose.Words.Vba](../../aspose.words.vba/)
* assemblea [Aspose.Words](../../)


