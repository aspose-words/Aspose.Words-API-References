---
title: Hyphenation.IsDictionaryRegistered
linktitle: IsDictionaryRegistered
articleTitle: IsDictionaryRegistered
second_title: Aspose.Words für .NET
description: Entdecken Sie die Silbentrennungsmethode IsDictionaryRegistered. Sie prüft, ob für Ihre Sprache ein Wörterbuch registriert ist, und stellt so eine korrekte Silbentrennung in Ihren Anwendungen sicher.
type: docs
weight: 30
url: /de/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

Rückgaben`FALSCH` wenn für die angegebene Sprache kein Wörterbuch registriert ist oder wenn das registrierte Wörterbuch Null ist,`WAHR` andernfalls.

```csharp
public static bool IsDictionaryRegistered(string language)
```

## Beispiele

Zeigt, wie ein Silbentrennungswörterbuch registriert wird.

```csharp
// Ein Silbentrennungswörterbuch enthält eine Liste von Zeichenfolgen, die Silbentrennungsregeln für die Sprache des Wörterbuchs definieren.
// Wenn ein Dokument Textzeilen enthält, in denen ein Wort aufgeteilt und in der nächsten Zeile fortgesetzt werden könnte,
// Bei der Silbentrennung wird die Zeichenfolgenliste des Wörterbuchs nach den Teilzeichenfolgen dieses Wortes durchsucht.
// Wenn das Wörterbuch eine Teilzeichenfolge enthält, wird das Wort durch die Silbentrennung auf zwei Zeilen aufgeteilt
// durch die Teilzeichenfolge und fügen Sie der ersten Hälfte einen Bindestrich hinzu.
// Registrieren Sie eine Wörterbuchdatei aus dem lokalen Dateisystem im Gebietsschema „de-CH“.
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Öffnen Sie ein Dokument mit Text, dessen Gebietsschema mit dem unseres Wörterbuchs übereinstimmt.
// und speichern Sie es in einem Speicherformat mit fester Seitenanzahl. Der Text in diesem Dokument wird mit Bindestrichen versehen.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Laden Sie das Dokument neu, nachdem Sie die Registrierung des Wörterbuchs aufgehoben haben.
// und speichern Sie es in einem anderen PDF, das keinen getrennten Text enthält.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Siehe auch

* class [Hyphenation](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
