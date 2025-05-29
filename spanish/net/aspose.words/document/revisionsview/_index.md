---
title: Document.RevisionsView
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words para .NET
description: ¡Gestiona fácilmente las revisiones de documentos! Elige entre versiones originales o actualizadas para una colaboración fluida y una mayor productividad.
type: docs
weight: 380
url: /es/net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Obtiene o establece un valor que indica si se debe trabajar con la versión original o revisada de un documento.

```csharp
public RevisionsView RevisionsView { get; set; }
```

## Observaciones

El valor predeterminado es .

## Ejemplos

Muestra cómo cambiar entre la vista revisada y la vista original de un documento.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// Ver el objeto del documento como si se hubieran aceptado todas las revisiones. Actualmente admite etiquetas de lista.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### Ver también

* enum [RevisionsView](../../revisionsview/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
