---
title: Document.UpdateActualReferenceMarks
linktitle: UpdateActualReferenceMarks
articleTitle: UpdateActualReferenceMarks
second_title: Aspose.Words para .NET
description: Actualice sin esfuerzo todas las notas al pie y notas finales de su documento con el método Document UpdateActualReferenceMarks, mejorando la precisión y la eficiencia.
type: docs
weight: 800
url: /es/net/aspose.words/document/updateactualreferencemarks/
---
## Document.UpdateActualReferenceMarks method

Actualiza el[`ActualReferenceMark`](../../../aspose.words.notes/footnote/actualreferencemark/) propiedad de todas las notas al pie y notas finales del documento.

```csharp
public void UpdateActualReferenceMarks()
```

## Observaciones

Actualizando campos ([`UpdateFields`](../updatefields/) ) puede ser necesario para obtener el resultado correcto.

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

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
