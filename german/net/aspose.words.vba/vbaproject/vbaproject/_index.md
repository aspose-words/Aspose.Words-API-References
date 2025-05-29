---
title: VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos ein neues VBA-Projekt mit unserem Konstruktor-Tool. Beginnen Sie Ihre Programmierreise mit einem leeren Projekt und lassen Sie Ihrer Kreativität freien Lauf!
type: docs
weight: 10
url: /de/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

Erstellt ein leeres[`VbaProject`](../) .

```csharp
public VbaProject()
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

* class [VbaProject](../)
* namensraum [Aspose.Words.Vba](../../../aspose.words.vba/)
* Montage [Aspose.Words](../../../)
