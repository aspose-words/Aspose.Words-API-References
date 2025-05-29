---
title: SaveOptions.UpdateLastPrintedProperty
linktitle: UpdateLastPrintedProperty
articleTitle: UpdateLastPrintedProperty
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihr Dokumentenmanagement mit SaveOptions UpdateLastPrintedProperty. Steuern Sie LastPrinted-Updates für effizientes Speichern und einen verbesserten Workflow.
type: docs
weight: 180
url: /de/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) Eigenschaft wird vor dem Speichern aktualisiert.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## Beispiele

Zeigt, wie die Eigenschaft „Zuletzt gedruckt“ eines Dokuments beim Speichern aktualisiert wird.

```csharp
Document doc = new Document();

DateTime lastPrinted = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.LastPrinted = lastPrinted;

// Dieses Flag bestimmt, ob das zuletzt gedruckte Datum, das eine integrierte Eigenschaft ist, aktualisiert wird.
// Wenn ja, dann das Datum des letzten Speichervorgangs des Dokuments
// wobei dieses als Parameter übergebene SaveOptions-Objekt als Druckdatum verwendet wird.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// In Microsoft Word 2003 finden Sie diese Eigenschaft über Datei -> Eigenschaften -> Statistik -> Gedruckt.
// Es kann auch im Hauptteil des Dokuments angezeigt werden, indem ein PRINTDATE-Feld verwendet wird.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Öffnen Sie das gespeicherte Dokument und überprüfen Sie dann den Wert der Eigenschaft.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
    Assert.AreNotEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
else
    Assert.AreEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
