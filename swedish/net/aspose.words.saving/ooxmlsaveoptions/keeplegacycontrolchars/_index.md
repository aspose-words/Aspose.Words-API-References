---
title: OoxmlSaveOptions.KeepLegacyControlChars
linktitle: KeepLegacyControlChars
articleTitle: KeepLegacyControlChars
second_title: Aspose.Words för .NET
description: OoxmlSaveOptions KeepLegacyControlChars fast egendom. Behåller originalrepresentationen av äldre kontrolltecken i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/
---
## OoxmlSaveOptions.KeepLegacyControlChars property

Behåller originalrepresentationen av äldre kontrolltecken.

```csharp
public bool KeepLegacyControlChars { get; set; }
```

## Exempel

Visar hur man stöder äldre kontrolltecken vid konvertering till .docx.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// När vi sparar dokumentet i ett OOXML-format kan vi skapa ett OoxmlSaveOptions-objekt
// och skicka det sedan till dokumentets sparmetod för att ändra hur vi sparar dokumentet.
// Ställ in egenskapen "KeepLegacyControlChars" till "true" för att bevara
// det äldre tecknet "ShortDateTime" när du sparar.
// Ställ in egenskapen "KeepLegacyControlChars" till "false" för att ta bort
// det äldre tecknet "ShortDateTime" från utdatadokumentet.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Se även

* class [OoxmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
