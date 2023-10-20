---
title: VbaProject.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words für .NET
description: VbaProject Clone methode. Führt eine Kopie des ausVbaProject  in C#.
type: docs
weight: 70
url: /de/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

Führt eine Kopie des aus[`VbaProject`](../) .

```csharp
public VbaProject Clone()
```

### Rückgabewert

Das Geklonte[`VbaProject`](../).

## Beispiele

Zeigt, wie man ein VBA-Projekt und -Modul tief klont.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// Im Zieldokument haben wir bereits ein Modul namens „Module1“
// weil wir es zusammen mit dem Projekt geklont haben. Wir müssen das Modul entfernen.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### Siehe auch

* class [VbaProject](../)
* namensraum [Aspose.Words.Vba](../../../aspose.words.vba/)
* Montage [Aspose.Words](../../../)
