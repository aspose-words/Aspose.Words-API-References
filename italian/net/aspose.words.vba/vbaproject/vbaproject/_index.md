---
title: VbaProject.VbaProject
second_title: Aspose.Words per .NET API Reference
description: VbaProject costruttore. Crea un VbaProject vuoto.
type: docs
weight: 10
url: /it/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

Crea un VbaProject vuoto.

```csharp
public VbaProject()
```

### Esempi

Mostra come creare un progetto VBA utilizzando le macro.

```csharp
Document doc = new Document();

// Crea un nuovo progetto VBA.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Crea un nuovo modulo e specifica un codice sorgente della macro.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Aggiunge il modulo al progetto VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Guarda anche

* class [VbaProject](../)
* spazio dei nomi [Aspose.Words.Vba](../../vbaproject/)
* assemblea [Aspose.Words](../../../)


