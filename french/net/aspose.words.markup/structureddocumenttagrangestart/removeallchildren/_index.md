---
title: StructuredDocumentTagRangeStart.RemoveAllChildren
second_title: Référence de l'API Aspose.Words pour .NET
description: StructuredDocumentTagRangeStart méthode. Supprime tous les nœuds entre ce nœud de début de plage et le nœud de fin de plage.
type: docs
weight: 230
url: /fr/net/aspose.words.markup/structureddocumenttagrangestart/removeallchildren/
---
## StructuredDocumentTagRangeStart.RemoveAllChildren method

Supprime tous les nœuds entre ce nœud de début de plage et le nœud de fin de plage.

```csharp
public void RemoveAllChildren()
```

### Exemples

Montre comment créer/supprimer une balise de document structuré et son contenu.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("StructuredDocumentTag element");

    InsertStructuredDocumentTagRanges(doc, out StructuredDocumentTagRangeStart rangeStart);

    // Supprime la balise de document structuré à distance, mais conserve le contenu à l'intérieur.
    rangeStart.RemoveSelfOnly();

    rangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(
        NodeType.StructuredDocumentTagRangeStart, 0, false);
    Assert.AreEqual(null, rangeStart);

    StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.GetChild(
        NodeType.StructuredDocumentTagRangeEnd, 0, false);

    Assert.AreEqual(null, rangeEnd);
    Assert.AreEqual("StructuredDocumentTag element", doc.GetText().Trim());

    InsertStructuredDocumentTagRanges(doc, out rangeStart);

    Node paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual("StructuredDocumentTag element", paragraphNode?.GetText().Trim());

    // Supprime la balise de document structuré à distance et le contenu à l'intérieur.
    rangeStart.RemoveAllChildren();

    paragraphNode = rangeStart.LastOrDefault();
    Assert.AreEqual(null, paragraphNode?.GetText());
}

public void InsertStructuredDocumentTagRanges(Document doc, out StructuredDocumentTagRangeStart rangeStart)
{
    rangeStart = new StructuredDocumentTagRangeStart(doc, SdtType.PlainText);
    StructuredDocumentTagRangeEnd rangeEnd = new StructuredDocumentTagRangeEnd(doc, rangeStart.Id);

    doc.FirstSection.Body.InsertBefore(rangeStart, doc.FirstSection.Body.FirstParagraph);
    doc.LastSection.Body.InsertAfter(rangeEnd, doc.FirstSection.Body.FirstParagraph);
}
```

### Voir également

* class [StructuredDocumentTagRangeStart](../)
* espace de noms [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* Assemblée [Aspose.Words](../../../)


