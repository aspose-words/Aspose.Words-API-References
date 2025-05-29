---
title: VbaProject.CodePage
linktitle: CodePage
articleTitle: CodePage
second_title: Aspose.Words per .NET
description: Scopri come gestire la proprietà CodePage di VbaProject per ottimizzare le impostazioni della code page del tuo progetto VBA, migliorando prestazioni e compatibilità.
type: docs
weight: 20
url: /it/net/aspose.words.vba/vbaproject/codepage/
---
## VbaProject.CodePage property

Ottiene o imposta la code page del progetto VBA.

```csharp
public int CodePage { get; set; }
```

## Osservazioni

Si noti che VBA è una funzionalità pre-Unicode e che è necessario impostare esplicitamente la code page appropriata per preservare i set di caratteri regionali.

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
