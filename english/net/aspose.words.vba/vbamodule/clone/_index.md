---
title: VbaModule.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: Effortlessly duplicate your VbaModule with the Clone method. Streamline your coding process and enhance productivity with this powerful feature.
type: docs
weight: 50
url: /net/aspose.words.vba/vbamodule/clone/
---
## VbaModule.Clone method

Performs a copy of the [`VbaModule`](../).

```csharp
public VbaModule Clone()
```

### Return Value

The cloned [`VbaModule`](../).

## Examples

Shows how to deep clone a VBA project and module.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// In the destination document, we already have a module named "Module1"
// because we cloned it along with the project. We will need to remove the module.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### See Also

* class [VbaModule](../)
* namespace [Aspose.Words.Vba](../../../aspose.words.vba/)
* assembly [Aspose.Words](../../../)
