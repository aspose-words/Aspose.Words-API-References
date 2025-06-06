---
title: VbaModuleType Enum
linktitle: VbaModuleType
articleTitle: VbaModuleType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Vba.VbaModuleType, che definisce i tipi di modello nei progetti VBA per un'automazione avanzata e una gestione semplificata dei documenti.
type: docs
weight: 7420
url: /it/net/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enumeration

Specifica il tipo di un modello in un progetto VBA.

```csharp
public enum VbaModuleType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| DocumentModule | `0` | Un tipo di elemento di progetto VBA che specifica un modulo per macro incorporate e operazioni di accesso programmatico associate a un documento. |
| ProceduralModule | `1` | Una raccolta di subroutine e funzioni. |
| ClassModule | `2` | Un modulo che contiene la definizione di un nuovo oggetto. Ogni istanza di una classe crea un nuovo oggetto, e le procedure definite nel modulo diventano proprietà e metodi dell'oggetto. |
| DesignerModule | `3` | Un modulo VBA che estende i metodi e le proprietà di un controllo ActiveX registrato nel progetto. |

## Esempi

Mostra come creare un progetto VBA utilizzando le macro.

```csharp
Document doc = new Document();

// Crea un nuovo progetto VBA.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Crea un nuovo modulo e specifica un codice sorgente macro.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Aggiungere il modulo al progetto VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Vba](../../aspose.words.vba/)
* assemblea [Aspose.Words](../../)
