---
title: FindReplaceOptions.MatchCase
second_title: Aspose.Words für .NET-API-Referenz
description: FindReplaceOptions eigendom. True gibt einen Vergleich unter Berücksichtigung der Groß/Kleinschreibung an false zeigt einen Vergleich ohne Berücksichtigung der Groß/Kleinschreibung an.
type: docs
weight: 140
url: /de/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

„True“ gibt einen Vergleich unter Berücksichtigung der Groß-/Kleinschreibung an, „false“ zeigt einen Vergleich ohne Berücksichtigung der Groß-/Kleinschreibung an.

```csharp
public bool MatchCase { get; set; }
```

### Beispiele

Zeigt, wie die Groß-/Kleinschreibung beim Durchführen eines Suchen-und-Ersetzen-Vorgangs umgeschaltet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Such- und Ersetzungsprozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das Flag „MatchCase“ auf „true“, um bei der Suche nach zu ersetzenden Zeichenfolgen die Groß-/Kleinschreibung zu berücksichtigen.
// Setzen Sie das Flag „MatchCase“ auf „false“, um die Groß-/Kleinschreibung bei der Suche nach zu ersetzendem Text zu ignorieren.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../findreplaceoptions/)
* Montage [Aspose.Words](../../../)


