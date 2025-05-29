---
title: VbaModule
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos leere VBA-Module mit unserem VbaModule-Konstruktor. Optimieren Sie Ihren Codierungsprozess und verbessern Sie Ihren Entwicklungsworkflow noch heute!
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

* class [VbaModule](../)
* namensraum [Aspose.Words.Vba](../../../aspose.words.vba/)
* Montage [Aspose.Words](../../../)
