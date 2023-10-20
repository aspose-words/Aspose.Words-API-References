---
title: Hyphenation.UnregisterDictionary
linktitle: UnregisterDictionary
articleTitle: UnregisterDictionary
second_title: Aspose.Words für .NET
description: Hyphenation UnregisterDictionary methode. Hebt die Registrierung eines Silbentrennungswörterbuchs für die angegebene Sprache auf in C#.
type: docs
weight: 50
url: /de/net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

Hebt die Registrierung eines Silbentrennungswörterbuchs für die angegebene Sprache auf.

Dies unterscheidet sich von der Registrierung eines Null-Wörterbuchs. Durch das Aufheben der Registrierung eines Wörterbuchs wird ein Rückruf für die angegebene Sprache aktiviert.

```csharp
public static void UnregisterDictionary(string language)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| language | String | Ein Sprachname, z. B. „en-US“. Weitere Informationen finden Sie in der .NET-Dokumentation für „Kulturname“ und RFC 4646. |

## Beispiele

Zeigt, wie man ein Silbentrennungswörterbuch registriert.

```csharp
// Ein Silbentrennungswörterbuch enthält eine Liste von Zeichenfolgen, die Silbentrennungsregeln für die Sprache des Wörterbuchs definieren.
// Wenn ein Dokument Textzeilen enthält, in denen ein Wort aufgeteilt und in der nächsten Zeile fortgesetzt werden könnte,
// Silbentrennung durchsucht die Zeichenfolgenliste des Wörterbuchs nach den Teilzeichenfolgen dieses Wortes.
// Wenn das Wörterbuch eine Teilzeichenfolge enthält, wird das Wort durch die Silbentrennung auf zwei Zeilen aufgeteilt
// durch die Teilzeichenfolge und fügen Sie einen Bindestrich in die erste Hälfte ein.
// Registrieren Sie eine Wörterbuchdatei aus dem lokalen Dateisystem im Gebietsschema „de-CH“.
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Öffnen Sie ein Dokument, das Text mit einem Gebietsschema enthält, das dem unseres Wörterbuchs entspricht.
// und in einem festen Seitenspeicherformat speichern. Der Text in diesem Dokument wird getrennt.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Laden Sie das Dokument erneut, nachdem Sie die Registrierung des Wörterbuchs aufgehoben haben.
// und speichern Sie es in einer anderen PDF-Datei, die keinen getrennten Text enthält.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Siehe auch

* class [Hyphenation](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
