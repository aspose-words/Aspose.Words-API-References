---
title: SaveOptions.UpdateLastPrintedProperty
second_title: Aspose.Words für .NET-API-Referenz
description: SaveOptions eigendom. Ruft einen Wert ab oder legt ihn fest der bestimmt ob dieLastPrinted Eigenschaft wird vor dem Speichern aktualisiert.
type: docs
weight: 180
url: /de/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) Eigenschaft wird vor dem Speichern aktualisiert.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

### Beispiele

Zeigt, wie die „CreatedTime“-Eigenschaft eines Dokuments beim Speichern aktualisiert wird.

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.CreatedTime = new DateTime(2019, 12, 20);

// Dieses Flag bestimmt, ob die erstellte Zeit, die eine eingebaute Eigenschaft ist, aktualisiert wird.
// Wenn ja, dann das Datum der letzten Speicheroperation des Dokuments
// mit diesem als Parameter übergebenen SaveOptions-Objekt wird als Erstellungszeit verwendet.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Öffnen Sie das gespeicherte Dokument und überprüfen Sie dann den Wert der Eigenschaft.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

Assert.AreNotEqual(isUpdateCreatedTimeProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.CreatedTime);
```

Zeigt, wie die Eigenschaft „Zuletzt gedruckt“ eines Dokuments beim Speichern aktualisiert wird.

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.LastPrinted = new DateTime(2019, 12, 20);

// Dieses Flag bestimmt, ob das letzte gedruckte Datum, das eine eingebaute Eigenschaft ist, aktualisiert wird.
// Wenn ja, dann das Datum der letzten Speicheroperation des Dokuments
// mit diesem als Parameter übergebenen SaveOptions-Objekt wird als Druckdatum verwendet.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// In Microsoft Word 2003 finden Sie diese Eigenschaft über Datei -> Eigenschaften -> Statistiken -> Gedruckt.
// Es kann auch im Hauptteil des Dokuments angezeigt werden, indem ein PRINTDATE-Feld verwendet wird.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Öffnen Sie das gespeicherte Dokument und überprüfen Sie dann den Wert der Eigenschaft.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

Assert.AreNotEqual(isUpdateLastPrintedProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.LastPrinted);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../saveoptions/)
* Montage [Aspose.Words](../../../)


