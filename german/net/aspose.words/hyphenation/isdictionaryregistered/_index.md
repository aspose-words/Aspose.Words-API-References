---
title: Hyphenation.IsDictionaryRegistered
linktitle: IsDictionaryRegistered
articleTitle: IsDictionaryRegistered
second_title: Aspose.Words für .NET
description: Hyphenation IsDictionaryRegistered methode. Gibt zurückFALSCH wenn für die angegebene Sprache kein Wörterbuch registriert ist oder wenn registriert ein NullWörterbuch istWAHR sonst in C#.
type: docs
weight: 30
url: /de/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

Gibt zurück`FALSCH` wenn für die angegebene Sprache kein Wörterbuch registriert ist oder wenn registriert ein Null-Wörterbuch ist,`WAHR` sonst.

```csharp
public static bool IsDictionaryRegistered(string language)
```

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
