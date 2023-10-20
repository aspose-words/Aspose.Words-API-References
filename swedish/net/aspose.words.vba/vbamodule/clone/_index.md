---
title: VbaModule.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words för .NET
description: VbaModule Clone metod. Utför en kopia avVbaModule  i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.vba/vbamodule/clone/
---
## VbaModule.Clone method

Utför en kopia av[`VbaModule`](../) .

```csharp
public VbaModule Clone()
```

### Returvärde

Den klonade[`VbaModule`](../).

## Exempel

Visar hur man djupklonar ett VBA-projekt och en modul.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// I destinationsdokumentet har vi redan en modul som heter "Module1"
// eftersom vi klonade det tillsammans med projektet. Vi kommer att behöva ta bort modulen.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### Se även

* class [VbaModule](../)
* namnutrymme [Aspose.Words.Vba](../../../aspose.words.vba/)
* hopsättning [Aspose.Words](../../../)
