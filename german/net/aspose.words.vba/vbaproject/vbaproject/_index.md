---
title: VbaProject.VbaProject
second_title: Aspose.Words für .NET-API-Referenz
description: VbaProject constructeur. Erstellt ein leeres VbaProject.
type: docs
weight: 10
url: /de/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

Erstellt ein leeres VbaProject.

```csharp
public VbaProject()
```

### Beispiele

Zeigt, wie ein VBA-Projekt mithilfe von Makros erstellt wird.

```csharp
Document doc = new Document();

// Erstellen Sie ein neues VBA-Projekt.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Erstellen Sie ein neues Modul und geben Sie einen Makroquellcode an.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Modul zum VBA-Projekt hinzufügen.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Siehe auch

* class [VbaProject](../)
* namensraum [Aspose.Words.Vba](../../vbaproject/)
* Montage [Aspose.Words](../../../)


