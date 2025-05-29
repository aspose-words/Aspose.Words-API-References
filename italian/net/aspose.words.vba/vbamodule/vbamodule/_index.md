---
title: VbaModule
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words per .NET
description: Crea senza sforzo moduli VBA vuoti con il nostro costruttore VbaModule. Semplifica il tuo processo di codifica e migliora il tuo flusso di lavoro di sviluppo oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule constructor

Crea un modulo vuoto.

```csharp
public VbaModule()
```

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

* class [VbaModule](../)
* spazio dei nomi [Aspose.Words.Vba](../../../aspose.words.vba/)
* assemblea [Aspose.Words](../../../)
