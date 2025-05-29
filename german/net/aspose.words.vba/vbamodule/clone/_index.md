---
title: VbaModule.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words für .NET
description: Duplizieren Sie Ihr VbaModule mühelos mit der Klonmethode. Optimieren Sie Ihren Codierungsprozess und steigern Sie Ihre Produktivität mit dieser leistungsstarken Funktion.
type: docs
weight: 50
url: /de/net/aspose.words.vba/vbamodule/clone/
---
## VbaModule.Clone method

Führt eine Kopie der[`VbaModule`](../) .

```csharp
public VbaModule Clone()
```

### Rückgabewert

Der geklonte[`VbaModule`](../).

## Beispiele

Zeigt, wie ein VBA-Projekt und -Modul tief geklont wird.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// Im Zieldokument haben wir bereits ein Modul mit dem Namen „Modul1“
// weil wir es zusammen mit dem Projekt geklont haben. Wir müssen das Modul entfernen.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### Siehe auch

* class [VbaModule](../)
* namensraum [Aspose.Words.Vba](../../../aspose.words.vba/)
* Montage [Aspose.Words](../../../)
