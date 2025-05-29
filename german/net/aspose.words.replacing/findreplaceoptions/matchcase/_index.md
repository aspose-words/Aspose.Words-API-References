---
title: FindReplaceOptions.MatchCase
linktitle: MatchCase
articleTitle: MatchCase
second_title: Aspose.Words für .NET
description: Entdecken Sie die MatchCase-Eigenschaft in FindReplaceOptions und aktivieren Sie Groß- und Kleinschreibungsvergleiche für präzise Textbearbeitung. Optimieren Sie Ihren Workflow!
type: docs
weight: 140
url: /de/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

„True“ bedeutet, dass beim Vergleich die Groß- und Kleinschreibung beachtet wird, „False“ bedeutet, dass beim Vergleich die Groß- und Kleinschreibung nicht beachtet wird.

```csharp
public bool MatchCase { get; set; }
```

## Beispiele

Zeigt, wie die Groß-/Kleinschreibung beim Ausführen einer Suchen-und-Ersetzen-Operation umgeschaltet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das Flag „MatchCase“ auf „true“, um beim Suchen nach zu ersetzenden Zeichenfolgen die Groß-/Kleinschreibung zu berücksichtigen.
// Setzen Sie das Flag „MatchCase“ auf „false“, um die Groß-/Kleinschreibung bei der Suche nach zu ersetzendem Text zu ignorieren.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
