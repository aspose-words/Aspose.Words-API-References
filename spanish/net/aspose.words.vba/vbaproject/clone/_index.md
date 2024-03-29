---
title: VbaProject.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words para .NET
description: VbaProject Clone método. Realiza una copia delVbaProject  en C#.
type: docs
weight: 70
url: /es/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

Realiza una copia del[`VbaProject`](../) .

```csharp
public VbaProject Clone()
```

### Valor_devuelto

el clonado[`VbaProject`](../).

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

* class [VbaProject](../)
* espacio de nombres [Aspose.Words.Vba](../../../aspose.words.vba/)
* asamblea [Aspose.Words](../../../)
