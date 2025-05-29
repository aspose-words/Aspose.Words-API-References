---
title: Footnote.ActualReferenceMark
linktitle: ActualReferenceMark
articleTitle: ActualReferenceMark
second_title: Aspose.Words para .NET
description: Descubra la propiedad Footnote ActualReferenceMark para acceder al texto preciso de las marcas de referencia en sus documentos, mejorando la claridad y la organización.
type: docs
weight: 20
url: /es/net/aspose.words.notes/footnote/actualreferencemark/
---
## Footnote.ActualReferenceMark property

Obtiene el texto real de la marca de referencia que se muestra en el documento para esta nota al pie.

```csharp
public string ActualReferenceMark { get; }
```

## Observaciones

Para completar inicialmente los valores de esta propiedad para todas las marcas de referencia del documento, o para actualizar los valores después de cambios en el documento que puedan afectar las marcas de referencia, debe ejecutar [`UpdateActualReferenceMarks`](../../../aspose.words/document/updateactualreferencemarks/) método. Actualizando campos ([`UpdateFields`](../../../aspose.words/document/updatefields/) ) también puede ser necesario para obtener el resultado correcto.

## Ejemplos

Muestra cómo obtener la marca de referencia de nota al pie real.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

Footnote footnote = (Footnote)doc.GetChild(NodeType.Footnote, 1, true);
doc.UpdateFields();
doc.UpdateActualReferenceMarks();

Assert.AreEqual("1", footnote.ActualReferenceMark);
```

### Ver también

* class [Footnote](../)
* espacio de nombres [Aspose.Words.Notes](../../../aspose.words.notes/)
* asamblea [Aspose.Words](../../../)
