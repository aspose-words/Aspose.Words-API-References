---
title: VbaModule.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words para .NET
description: VbaModule Clone método. Realiza una copia delVbaModule  en C#.
type: docs
weight: 50
url: /es/net/aspose.words.vba/vbamodule/clone/
---
## VbaModule.Clone method

Realiza una copia del[`VbaModule`](../) .

```csharp
public VbaModule Clone()
```

### Valor_devuelto

el clonado[`VbaModule`](../).

## Ejemplos

Muestra cómo realizar una clonación profunda de un proyecto y módulo de VBA.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// En el documento de destino ya tenemos un módulo llamado "Módulo1"
// porque lo clonamos junto con el proyecto. Tendremos que quitar el módulo.
VbaModule oldVbaModule = destDoc.VbaProject.Modules["Module1"];
VbaModule copyVbaModule = doc.VbaProject.Modules["Module1"].Clone();
destDoc.VbaProject.Modules.Remove(oldVbaModule);
destDoc.VbaProject.Modules.Add(copyVbaModule);

destDoc.Save(ArtifactsDir + "VbaProject.CloneVbaProject.docm");
```

### Ver también

* class [VbaModule](../)
* espacio de nombres [Aspose.Words.Vba](../../../aspose.words.vba/)
* asamblea [Aspose.Words](../../../)
