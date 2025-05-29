---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.FindReplaceOptions für erweiterte Such- und Ersetzungsfunktionen, die die Dokumentbearbeitung präziser und flexibler machen.
type: docs
weight: 5350
url: /de/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Gibt Optionen für Such-/Ersetzungsvorgänge an.

Um mehr zu erfahren, besuchen Sie die[Suchen und Ersetzen](https://docs.aspose.com/words/net/find-and-replace/) Dokumentationsartikel.

```csharp
public class FindReplaceOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Initialisiert eine neue Instanz der Klasse FindReplaceOptions mit Standardeinstellungen. |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) | Initialisiert eine neue Instanz der Klasse FindReplaceOptions mit der angegebenen Richtung. |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) | Initialisiert eine neue Instanz der FindReplaceOptions-Klasse mit dem angegebenen Ersetzungs-Callback. |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) | Initialisiert eine neue Instanz der Klasse FindReplaceOptions mit der angegebenen Richtung und dem Ersetzungs-Callback. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Textformatierung auf neuen Inhalt angewendet. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Absatzformatierung auf neuen Inhalt angewendet. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Wählt die Richtung für das Ersetzen. Der Standardwert istForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | „True“ bedeutet, dass der alte Wert ein eigenständiges Wort sein muss. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in gelöschten Revisionen ignoriert werden soll. Der Standardwert ist`FALSCH` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in Feldcodes ignoriert werden soll. Der Standardwert ist`FALSCH` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in Feldern ignoriert werden soll. Der Standardwert ist`FALSCH` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Fußnoten ignoriert werden sollen. Der Standardwert ist`FALSCH` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in eingefügten Revisionen ignoriert werden soll. Der Standardwert ist`FALSCH` . |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Formen innerhalb eines Textes ignoriert werden sollen. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | Ruft einen booleschen Wert ab oder setzt ihn, der angibt, ob der Inhalt von[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) . Der Standardwert ist`FALSCH` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, dass der alte Suchen/Ersetzen-Algorithmus verwendet wird. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | „True“ bedeutet, dass beim Vergleich die Groß- und Kleinschreibung beachtet wird, „False“ bedeutet, dass beim Vergleich die Groß- und Kleinschreibung nicht beachtet wird. |
| [ReplacementFormat](../../aspose.words.replacing/findreplaceoptions/replacementformat/) { get; set; } | Gibt das Format des Ersatzes an. Standard istText . |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | Die benutzerdefinierte Methode, die vor jedem Ersetzungsvorgang aufgerufen wird. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Ruft einen Booleschen Wert ab oder legt ihn fest, der angibt, ob der Absatz „break “ ersetzt werden darf, wenn kein nächster gleichgeordneter Absatz vorhanden ist. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True gibt an, dass eine Textsuche sequenziell von oben nach unten unter Berücksichtigung der Textfelder durchgeführt wird. Der Standardwert ist`FALSCH` . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Ersetzungen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen. Der Standardwert ist`FALSCH` . |

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

Zeigt, wie eigenständige Such- und Ersetzungsvorgänge nur für Wörter umgeschaltet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das Flag „FindWholeWordsOnly“ auf „true“, um den gefundenen Text zu ersetzen, wenn er nicht Teil eines anderen Wortes ist.
// Setzen Sie das Flag „FindWholeWordsOnly“ auf „false“, um den gesamten Text unabhängig von seiner Umgebung zu ersetzen.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Siehe auch

* namensraum [Aspose.Words.Replacing](../../aspose.words.replacing/)
* Montage [Aspose.Words](../../)
