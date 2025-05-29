---
title: VbaModule.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die VbaModule-Typ-Eigenschaft und definieren Sie Ihre Module als prozedural, Dokument, Klasse oder Designer für verbesserte Funktionalität und Organisation.
type: docs
weight: 40
url: /de/net/aspose.words.vba/vbamodule/type/
---
## VbaModule.Type property

Gibt an, ob das Modul ein prozedurales Modul, ein Dokumentmodul, ein Klassenmodul oder ein Designermodul ist.

```csharp
public VbaModuleType Type { get; set; }
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

* enum [VbaModuleType](../../vbamoduletype/)
* class [VbaModule](../)
* namensraum [Aspose.Words.Vba](../../../aspose.words.vba/)
* Montage [Aspose.Words](../../../)
