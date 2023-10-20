---
title: VbaModule.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words per .NET
description: VbaModule Clone metodo. Esegue una copia del fileVbaModule  in C#.
type: docs
weight: 50
url: /it/net/aspose.words.vba/vbamodule/clone/
---
## VbaModule.Clone method

Esegue una copia del file[`VbaModule`](../) .

```csharp
public VbaModule Clone()
```

### Valore di ritorno

Il clonato[`VbaModule`](../).

## Esempi

Mostra come clonare in profondità un progetto e un modulo VBA.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// Nel documento di destinazione abbiamo già un modulo chiamato "Module1"
// perché lo abbiamo clonato insieme al progetto. Dovremo rimuovere il modulo.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### Guarda anche

* class [VbaModule](../)
* spazio dei nomi [Aspose.Words.Vba](../../../aspose.words.vba/)
* assemblea [Aspose.Words](../../../)
