---
title: VbaModule.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words för .NET
description: Duplicera enkelt din VbaModule med kloningsmetoden. Effektivisera din kodningsprocess och öka produktiviteten med denna kraftfulla funktion.
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

// I destinationsdokumentet har vi redan en modul med namnet "Modul1"
// eftersom vi klonade den tillsammans med projektet. Vi kommer att behöva ta bort modulen.
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
