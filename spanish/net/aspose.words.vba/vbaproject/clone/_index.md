---
title: VbaProject.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words para .NET
description: Duplica fácilmente tu VBAProject con el método Clonar. ¡Mejora tu flujo de trabajo y optimiza la gestión de proyectos hoy mismo!
type: docs
weight: 80
url: /es/net/aspose.words.vba/vbaproject/clone/
---
## VbaProject.Clone method

Realiza una copia del[`VbaProject`](../) .

```csharp
public VbaProject Clone()
```

### Valor_devuelto

El clonado[`VbaProject`](../).

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

* class [VbaProject](../)
* espacio de nombres [Aspose.Words.Vba](../../../aspose.words.vba/)
* asamblea [Aspose.Words](../../../)
