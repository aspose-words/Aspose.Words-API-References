---
title: OoxmlSaveOptions.KeepLegacyControlChars
second_title: Aspose.Words für .NET-API-Referenz
description: OoxmlSaveOptions eigendom. Behält die ursprüngliche Darstellung der alten Steuerzeichen bei.
type: docs
weight: 40
url: /de/net/aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/
---
## OoxmlSaveOptions.KeepLegacyControlChars property

Behält die ursprüngliche Darstellung der alten Steuerzeichen bei.

```csharp
public bool KeepLegacyControlChars { get; set; }
```

### Beispiele

Zeigt, wie ältere Steuerzeichen bei der Konvertierung in .docx unterstützt werden.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Wenn wir das Dokument in einem OOXML-Format speichern, können wir ein OoxmlSaveOptions-Objekt erstellen
// und übergeben Sie es dann an die Speichermethode des Dokuments, um zu ändern, wie wir das Dokument speichern.
// Setzen Sie die Eigenschaft „KeepLegacyControlChars“ auf „true“, um sie beizubehalten
// das Legacy-Zeichen „ShortDateTime“ beim Speichern.
// Setzen Sie die Eigenschaft „KeepLegacyControlChars“ zum Entfernen auf „false“.
// das „ShortDateTime“-Legacy-Zeichen aus dem Ausgabedokument.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Siehe auch

* class [OoxmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* Montage [Aspose.Words](../../../)


