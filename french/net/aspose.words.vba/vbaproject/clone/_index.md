---
title: Clone
second_title: Référence de l'API Aspose.Words pour .NET
description: Effectue une copie duVbaProjectaspose.words.vba/vbaproject .
type: docs
weight: 70
url: /fr/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

Effectue une copie du[`VbaProject`](../../vbaproject) .

```csharp
public VbaProject Clone()
```

### Return_Value

Le VbaProject cloné.

### Exemples

Montre comment cloner en profondeur un projet et un module VBA.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// Dans le document de destination, nous avons déjà un module nommé "Module1"
// parce que nous l'avons cloné avec le projet. Nous devrons supprimer le module.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### Voir également

* class [VbaProject](../../vbaproject)
* espace de noms [Aspose.Words.Vba](../../vbaproject)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->