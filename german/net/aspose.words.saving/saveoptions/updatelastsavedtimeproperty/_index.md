---
title: SaveOptions.UpdateLastSavedTimeProperty
second_title: Aspose.Words für .NET-API-Referenz
description: SaveOptions eigendom. Ruft einen Wert ab oder legt ihn fest der bestimmt ob dieLastSavedTime Eigenschaft wird vor dem Speichern aktualisiert.
type: docs
weight: 180
url: /de/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) Eigenschaft wird vor dem Speichern aktualisiert.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

### Beispiele

Zeigt, wie Sie bestimmen können, ob die Eigenschaft „Zuletzt gespeicherte Zeit“ des Dokuments beim Speichern beibehalten werden soll.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// Wenn wir das Dokument in einem OOXML-Format speichern, können wir ein OoxmlSaveOptions-Objekt erstellen
// und übergeben Sie es dann an die Speichermethode des Dokuments, um zu ändern, wie wir das Dokument speichern.
// Setzen Sie die Eigenschaft „UpdateLastSavedTimeProperty“ auf „true“.
// die integrierte Eigenschaft „Letzte gespeicherte Zeit“ des Ausgabedokuments auf das aktuelle Datum/die aktuelle Uhrzeit setzen.
// Die Eigenschaft „UpdateLastSavedTimeProperty“ auf „false“ setzen
// Den ursprünglichen Wert der integrierten Eigenschaft „Letzte gespeicherte Zeit“ des Eingabedokuments beibehalten.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.That(DateTime.Now, Is.EqualTo(lastSavedTimeNew).Within(1).Days);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../saveoptions/)
* Montage [Aspose.Words](../../../)


