---
title: VbaModuleCollection.Add
second_title: Aspose.Words für .NET-API-Referenz
description: VbaModuleCollection methode. Fügt der Sammlung ein Modul hinzu.
type: docs
weight: 30
url: /de/net/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection.Add method

Fügt der Sammlung ein Modul hinzu.

```csharp
public void Add(VbaModule vbaModule)
```

### Beispiele

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* namensraum [Aspose.Words.Vba](../../vbamodulecollection/)
* Montage [Aspose.Words](../../../)


