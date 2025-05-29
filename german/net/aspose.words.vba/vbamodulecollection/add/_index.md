---
title: VbaModuleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre VBA-Projekte mühelos mit der VbaModuleCollection-Add-Methode, die das nahtlose Hinzufügen von Modulen für eine verbesserte Funktionalität ermöglicht.
type: docs
weight: 30
url: /de/net/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection.Add method

Fügt der Sammlung ein Modul hinzu.

```csharp
public void Add(VbaModule vbaModule)
```

## Beispiele

Zeigt, wie man mit Makros ein VBA-Projekt erstellt.

```csharp
Document doc = new Document();

// Erstellen Sie ein neues VBA-Projekt.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Erstellen Sie ein neues Modul und geben Sie einen Makro-Quellcode an.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Fügen Sie das Modul zum VBA-Projekt hinzu.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Siehe auch

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* namensraum [Aspose.Words.Vba](../../../aspose.words.vba/)
* Montage [Aspose.Words](../../../)
