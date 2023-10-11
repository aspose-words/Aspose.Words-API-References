---
title: VbaModule.VbaModule
second_title: Aspose.Words per .NET API Reference
description: VbaModule costruttore. Crea un modulo vuoto.
type: docs
weight: 10
url: /it/net/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule constructor

Crea un modulo vuoto.

```csharp
public VbaModule()
```

### Esempi

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

// Aggiunge il modulo al progetto VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Guarda anche

* class [VbaModule](../)
* spazio dei nomi [Aspose.Words.Vba](../../vbamodule/)
* assemblea [Aspose.Words](../../../)


