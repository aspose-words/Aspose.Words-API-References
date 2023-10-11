---
title: VbaModule.Clone
second_title: Référence de l'API Aspose.Words pour .NET
description: VbaModule méthode. Effectue une copie duVbaModule .
type: docs
weight: 50
url: /fr/net/aspose.words.vba/vbamodule/clone/
---
## VbaModule.Clone method

Effectue une copie du[`VbaModule`](../) .

```csharp
public VbaModule Clone()
```

### Return_Value

Le cloné[`VbaModule`](../).

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

* class [VbaModule](../)
* espace de noms [Aspose.Words.Vba](../../vbamodule/)
* Assemblée [Aspose.Words](../../../)


