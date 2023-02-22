---
title: Section.DeleteHeaderFooterShapes
second_title: Référence de l'API Aspose.Words pour .NET
description: Section méthode. Supprime toutes les formes objets de dessin des entêtes et pieds de page de cette section.
type: docs
weight: 120
url: /fr/net/aspose.words/section/deleteheaderfootershapes/
---
## Section.DeleteHeaderFooterShapes method

Supprime toutes les formes (objets de dessin) des en-têtes et pieds de page de cette section.

```csharp
public void DeleteHeaderFooterShapes()
```

### Exemples

Montre comment supprimer toutes les formes de tous les en-têtes et pieds de page d'une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crée un en-tête principal avec une forme.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.InsertShape(ShapeType.Rectangle, 100, 100);

// Crée un pied de page principal avec une image.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.InsertImage(ImageDir + "Logo Icon.ico");

Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);

// Supprime toutes les formes des en-têtes et pieds de page de la première section.
doc.FirstSection.DeleteHeaderFooterShapes();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);
```

### Voir également

* class [Section](../)
* espace de noms [Aspose.Words](../../section/)
* Assemblée [Aspose.Words](../../../)


