---
title: Section.DeleteHeaderFooterShapes
linktitle: DeleteHeaderFooterShapes
articleTitle: DeleteHeaderFooterShapes
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos alle Zeichnungsformen aus Abschnittskopf- und -fußzeilen mit der Methode „DeleteHeaderFooterShapes“, um eine übersichtlichere Dokumentdarstellung zu erzielen.
type: docs
weight: 140
url: /de/net/aspose.words/section/deleteheaderfootershapes/
---
## Section.DeleteHeaderFooterShapes method

Löscht alle Formen (Zeichenobjekte) aus den Kopf- und Fußzeilen dieses Abschnitts.

```csharp
public void DeleteHeaderFooterShapes()
```

## Beispiele

Zeigt, wie alle Formen aus allen Kopf- und Fußzeilen in einem Abschnitt entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine primäre Kopfzeile mit einer Form.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.InsertShape(ShapeType.Rectangle, 100, 100);

// Erstellen Sie eine primäre Fußzeile mit einem Bild.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.InsertImage(ImageDir + "Logo icon.ico");

Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);

// Entfernen Sie alle Formen aus den Kopf- und Fußzeilen im ersten Abschnitt.
doc.FirstSection.DeleteHeaderFooterShapes();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(0, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetChildNodes(NodeType.Shape, true).Count);
```

### Siehe auch

* class [Section](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
