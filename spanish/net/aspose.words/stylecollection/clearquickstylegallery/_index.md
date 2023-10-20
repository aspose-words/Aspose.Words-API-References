---
title: StyleCollection.ClearQuickStyleGallery
linktitle: ClearQuickStyleGallery
articleTitle: ClearQuickStyleGallery
second_title: Aspose.Words para .NET
description: StyleCollection ClearQuickStyleGallery método. Elimina todos los estilos del panel Galería de estilos rápidos en C#.
type: docs
weight: 80
url: /es/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Elimina todos los estilos del panel Galería de estilos rápidos.

```csharp
public void ClearQuickStyleGallery()
```

## Ejemplos

Muestra cómo eliminar estilos del panel Galería de estilos.

```csharp
Document doc = new Document();
// Tenga en cuenta que los estilos de eliminación solo funcionan con el formato DOCX por ahora.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Ver también

* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
