---
title: VbaModule.Type
second_title: Aspose.Words für .NET-API-Referenz
description: VbaModule eigendom. Gibt an ob das Modul ein prozedurales Modul Dokumentmodul Klassenmodul oder Designermodul ist.
type: docs
weight: 40
url: /de/net/aspose.words.vba/vbamodule/type/
---
## VbaModule.Type property

Gibt an, ob das Modul ein prozedurales Modul, Dokumentmodul, Klassenmodul oder Designermodul ist.

```csharp
public VbaModuleType Type { get; set; }
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

* enum [VbaModuleType](../../vbamoduletype/)
* class [VbaModule](../)
* namensraum [Aspose.Words.Vba](../../vbamodule/)
* Montage [Aspose.Words](../../../)


