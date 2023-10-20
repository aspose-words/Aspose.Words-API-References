---
title: VbaModule.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: VbaModule Type proprietà. Specifica se il modulo è un modulo procedurale un modulo di documento un modulo di classe o un modulo di progettazione in C#.
type: docs
weight: 40
url: /it/net/aspose.words.vba/vbamodule/type/
---
## VbaModule.Type property

Specifica se il modulo è un modulo procedurale, un modulo di documento, un modulo di classe o un modulo di progettazione.

```csharp
public VbaModuleType Type { get; set; }
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

// Aggiunge il modulo al progetto VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Guarda anche

* enum [VbaModuleType](../../vbamoduletype/)
* class [VbaModule](../)
* spazio dei nomi [Aspose.Words.Vba](../../../aspose.words.vba/)
* assemblea [Aspose.Words](../../../)
