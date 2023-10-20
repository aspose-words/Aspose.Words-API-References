---
title: VbaModule
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words für .NET
description: VbaModule constructeur. Erstellt ein leeres Modul in C#.
type: docs
weight: 10
url: /de/net/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule constructor

Erstellt ein leeres Modul.

```csharp
public VbaModule()
```

## Beispiele

Zeigt, wie man ein VBA-Projekt mithilfe von Makros erstellt.

```csharp
Document doc = new Document();

// Ein neues VBA-Projekt erstellen.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Ein neues Modul erstellen und einen Makroquellcode angeben.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Modul zum VBA-Projekt hinzufügen.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Siehe auch

* class [VbaModule](../)
* namensraum [Aspose.Words.Vba](../../../aspose.words.vba/)
* Montage [Aspose.Words](../../../)
