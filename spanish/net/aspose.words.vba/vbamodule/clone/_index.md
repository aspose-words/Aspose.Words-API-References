---
title: VbaModule.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words para .NET
description: Duplica fácilmente tu VbaModule con el método Clonar. Optimiza tu proceso de codificación y mejora tu productividad con esta potente función.
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

El clonado[`VbaModule`](../).

## Ejemplos

Muestra cómo clonar en profundidad un proyecto y un módulo VBA.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");
Document destDoc = new Document();

VbaProject copyVbaProject = doc.VbaProject.Clone();
destDoc.VbaProject = copyVbaProject;

// En el documento de destino, ya tenemos un módulo llamado "Módulo1"
// Porque lo clonamos junto con el proyecto. Tendremos que eliminar el módulo.
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
