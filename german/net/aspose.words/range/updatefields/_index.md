---
title: Range.UpdateFields
second_title: Aspose.Words für .NET-API-Referenz
description: Range methode. Aktualisiert die Werte der Dokumentfelder in diesem Bereich.
type: docs
weight: 110
url: /de/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Aktualisiert die Werte der Dokumentfelder in diesem Bereich.

```csharp
public void UpdateFields()
```

### Bemerkungen

Wenn Sie ein Dokument öffnen, ändern und dann speichern, aktualisiert Aspose.Words Felder nicht automatisch, sondern behält sie bei. Daher sollten Sie diese Methode normalerweise vor dem Speichern aufrufen, wenn Sie das Dokument programmgesteuert geändert haben und sicherstellen möchten die richtigen (berechneten) Feldwerte erscheinen im gespeicherten Dokument.

Es ist nicht erforderlich, Felder nach dem Ausführen eines Seriendrucks zu aktualisieren, da der Seriendruck eine Art Feldaktualisierung ist und automatisch alle Felder im Dokument aktualisiert.

Diese Methode aktualisiert nicht alle Feldtypen. Eine detaillierte Liste der unterstützten Feldtypen finden Sie im Programmierhandbuch.

Diese Methode aktualisiert keine Felder, die sich auf die Seitenlayout-Algorithmen beziehen (z. B. PAGE, PAGES, PAGEREF). Die Seitenlayout-bezogenen Felder werden aktualisiert, wenn Sie ein Dokument rendern oder aufrufen[`UpdatePageLayout`](../../document/updatepagelayout/).

Verwenden Sie zum Aktualisieren von Feldern im gesamten Dokument[`UpdateFields`](../../document/updatefields/).

### Beispiele

Zeigt, wie alle Felder in einem Bereich aktualisiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// Die obigen DOCPROPERTY-Felder zeigen den Wert dieser integrierten Dokumenteigenschaft an.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// Wenn wir den Wert einer Dokumenteigenschaft aktualisieren, müssen wir alle DOCPROPERTY-Felder aktualisieren, um ihn anzuzeigen.
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

// Alle Felder aktualisieren, die im Bereich des ersten Abschnitts liegen.
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### Siehe auch

* class [Range](../)
* namensraum [Aspose.Words](../../range/)
* Montage [Aspose.Words](../../../)


