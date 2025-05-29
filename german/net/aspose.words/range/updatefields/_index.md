---
title: Range.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Dokumente mühelos mit der Methode „Range UpdateFields“, indem Sie Feldwerte schnell und effizient aktualisieren und so die Genauigkeit verbessern.
type: docs
weight: 130
url: /de/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Aktualisiert die Werte der Dokumentfelder in diesem Bereich.

```csharp
public void UpdateFields()
```

## Bemerkungen

Wenn Sie ein Dokument öffnen, ändern und dann speichern, aktualisiert Aspose.Words die Felder nicht automatisch, sondern lässt sie unverändert. Daher möchten Sie diese Methode normalerweise vor dem Speichern aufrufen, wenn Sie das Dokument programmgesteuert geändert haben und sicherstellen möchten, dass die richtigen (berechneten) Feldwerte im gespeicherten Dokument angezeigt werden.

Es besteht keine Notwendigkeit, Felder nach der Ausführung eines Serienbriefs zu aktualisieren, da der Serienbrief eine Art Feldaktualisierung ist und alle Felder im Dokument automatisch aktualisiert.

Diese Methode aktualisiert nicht alle Feldtypen. Eine detaillierte Liste der unterstützten Feldtypen finden Sie im Programmierhandbuch.

Diese Methode aktualisiert keine Felder, die mit den Seitenlayout-Algorithmen in Zusammenhang stehen (z. B. PAGE, PAGES, PAGEREF). Die mit dem Seitenlayout in Zusammenhang stehenden Felder werden aktualisiert, wenn Sie ein Dokument rendern oder aufrufen[`UpdatePageLayout`](../../document/updatepagelayout/).

Um Felder im gesamten Dokument zu aktualisieren, verwenden Sie[`UpdateFields`](../../document/updatefields/).

## Beispiele

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

// Aktualisieren Sie alle Felder, die im Bereich des ersten Abschnitts liegen.
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### Siehe auch

* class [Range](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
