---
title: OoxmlSaveOptions.KeepLegacyControlChars
linktitle: KeepLegacyControlChars
articleTitle: KeepLegacyControlChars
second_title: Aspose.Words für .NET
description: Entdecken Sie die KeepLegacyControlChars-Eigenschaft von OoxmlSaveOptions, um das ursprüngliche Format älterer Steuerzeichen für eine nahtlose Dokumentkonvertierung beizubehalten.
type: docs
weight: 50
url: /de/net/aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/
---
## OoxmlSaveOptions.KeepLegacyControlChars property

Behält die ursprüngliche Darstellung der alten Steuerzeichen bei.

```csharp
public bool KeepLegacyControlChars { get; set; }
```

## Beispiele

Zeigt, wie ältere Steuerzeichen bei der Konvertierung in .docx unterstützt werden.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Wenn wir das Dokument in einem OOXML-Format speichern, können wir ein OoxmlSaveOptions-Objekt erstellen
// und übergeben Sie es dann an die Speichermethode des Dokuments, um zu ändern, wie wir das Dokument speichern.
// Setzen Sie die Eigenschaft "KeepLegacyControlChars" auf "true", um
// das Legacy-Zeichen „ShortDateTime“ beim Speichern.
// Setzen Sie die Eigenschaft "KeepLegacyControlChars" auf "false", um
// das Legacy-Zeichen „ShortDateTime“ aus dem Ausgabedokument.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Siehe auch

* class [OoxmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
