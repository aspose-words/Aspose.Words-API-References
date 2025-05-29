---
title: Document.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words para .NET
description: Mejore sin esfuerzo sus documentos con el método RemoveBlankPages, eliminando páginas en blanco no deseadas para lograr un acabado pulido y profesional.
type: docs
weight: 700
url: /es/net/aspose.words/document/removeblankpages/
---
## Document.RemoveBlankPages method

Elimina páginas en blanco del documento.

```csharp
public List<int> RemoveBlankPages()
```

### Valor_devuelto

La lista de números de página se consideró en blanco y se eliminó.

## Observaciones

El documento resultante no contendrá páginas consideradas como en blanco mientras que el resto del contenido, incluida la numeración, los encabezados/pies de página y el diseño general, debe permanecer sin cambios. Una página se considera en blanco cuando el cuerpo de la página no tiene contenido visible, por ejemplo, una tabla vacía que no tenga bordes se considerará invisible y, por lo tanto, la página se detectará como en blanco.

## Ejemplos

Muestra cómo eliminar páginas en blanco del documento.

```csharp
Document doc = new Document(MyDir + "Blank pages.docx");
Assert.AreEqual(2, doc.PageCount);
doc.RemoveBlankPages();
doc.UpdatePageLayout();
Assert.AreEqual(1, doc.PageCount);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
