---
title: StyleCollection.ClearQuickStyleGallery
second_title: Referencia de API de Aspose.Words para .NET
description: StyleCollection método. Elimina todos los estilos del panel Galería de estilos rápidos.
type: docs
weight: 80
url: /es/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Elimina todos los estilos del panel Galería de estilos rápidos.

```csharp
public void ClearQuickStyleGallery()
```

### Ejemplos

Muestra cómo eliminar estilos del panel Galería de estilos.

```csharp
Document doc = new Document();

// Tenga en cuenta que la eliminación de estilos solo funciona con el formato DOCX por ahora.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Ver también

* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../stylecollection/)
* asamblea [Aspose.Words](../../../)


