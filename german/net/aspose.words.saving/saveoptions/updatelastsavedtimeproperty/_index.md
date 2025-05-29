---
title: SaveOptions.UpdateLastSavedTimeProperty
linktitle: UpdateLastSavedTimeProperty
articleTitle: UpdateLastSavedTimeProperty
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre SaveOptions mit der UpdateLastSavedTimeProperty. Steuern Sie LastSavedTime-Updates für effizientes Datenmanagement und verbesserte Leistung.
type: docs
weight: 190
url: /de/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) Eigenschaft wird vor dem Speichern aktualisiert.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

## Beispiele

Zeigt, wie Sie bestimmen, ob die Eigenschaft „Zuletzt gespeicherter Zeitpunkt“ des Dokuments beim Speichern beibehalten werden soll.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// Wenn wir das Dokument in einem OOXML-Format speichern, können wir ein OoxmlSaveOptions-Objekt erstellen
// und übergeben Sie es dann an die Speichermethode des Dokuments, um zu ändern, wie wir das Dokument speichern.
// Setzen Sie die Eigenschaft "UpdateLastSavedTimeProperty" auf "true", um
// Setzen Sie die integrierte Eigenschaft „Zuletzt gespeicherte Zeit“ des Ausgabedokuments auf das aktuelle Datum/die aktuelle Uhrzeit.
// Setzen Sie die Eigenschaft "UpdateLastSavedTimeProperty" auf "false", um
// Bewahren Sie den ursprünglichen Wert der integrierten Eigenschaft „Zuletzt gespeicherter Zeitpunkt“ des Eingabedokuments auf.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.IsTrue((DateTime.Now - lastSavedTimeNew).Days < 1);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
