---
title: Enum RevisionsView
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.RevisionsView enumeración. Permite especificar si se trabaja con la versión original o revisada de un documento.
type: docs
weight: 4810
url: /es/net/aspose.words/revisionsview/
---
## RevisionsView enumeration

Permite especificar si se trabaja con la versión original o revisada de un documento.

```csharp
public enum RevisionsView
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Original | `0` | Especifica la versión original de un documento. |
| Final | `1` | Especifica la versión revisada de un documento. |

### Ejemplos

Muestra cómo cambiar entre la vista revisada y original de un documento.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Ver el objeto del documento como si se aceptaran todas las revisiones. Actualmente admite etiquetas de lista.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


