---
title: VbaProject.VbaProject
second_title: Aspose.Words für .NET-API-Referenz
description: VbaProject constructeur. Erstellt ein LeerzeichenVbaProject .
type: docs
weight: 10
url: /de/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

Erstellt ein Leerzeichen[`VbaProject`](../) .

```csharp
public VbaProject()
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

* class [VbaProject](../)
* namensraum [Aspose.Words.Vba](../../vbaproject/)
* Montage [Aspose.Words](../../../)


