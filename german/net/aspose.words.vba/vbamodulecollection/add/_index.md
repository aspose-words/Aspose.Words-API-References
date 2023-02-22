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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* namensraum [Aspose.Words.Vba](../../vbamodulecollection/)
* Montage [Aspose.Words](../../../)


