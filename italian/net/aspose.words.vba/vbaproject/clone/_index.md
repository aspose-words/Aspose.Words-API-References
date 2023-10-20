---
title: VbaProject.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words per .NET
description: VbaProject Clone metodo. Esegue una copia del fileVbaProject  in C#.
type: docs
weight: 70
url: /it/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

Esegue una copia del file[`VbaProject`](../) .

```csharp
public VbaProject Clone()
```

### Valore di ritorno

Il clonato[`VbaProject`](../).

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

* class [VbaProject](../)
* spazio dei nomi [Aspose.Words.Vba](../../../aspose.words.vba/)
* assemblea [Aspose.Words](../../../)
