---
title: VbaModule.Type
second_title: Aspose.Words für .NET-API-Referenz
description: VbaModule eigendom. Gibt an ob das Modul ein prozedurales Modul ein Dokumentmodul ein Klassenmodul oder ein Designermodul ist.
type: docs
weight: 40
url: /de/net/aspose.words.vba/vbamodule/type/
---
## VbaModule.Type property

Gibt an, ob das Modul ein prozedurales Modul, ein Dokumentmodul, ein Klassenmodul oder ein Designermodul ist.

```csharp
public VbaModuleType Type { get; set; }
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

* enum [VbaModuleType](../../vbamoduletype/)
* class [VbaModule](../)
* namensraum [Aspose.Words.Vba](../../vbamodule/)
* Montage [Aspose.Words](../../../)


