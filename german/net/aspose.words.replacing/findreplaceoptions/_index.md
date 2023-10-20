---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words für .NET
description: Aspose.Words.Replacing.FindReplaceOptions klas. Gibt Optionen für Such/Ersetzungsvorgänge an in C#.
type: docs
weight: 4620
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
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Default_Constructor |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) |  |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Textformatierung wird auf neue Inhalte angewendet. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Absatzformatierung wird auf neuen Inhalt angewendet. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Wählt die Richtung zum Ersetzen aus. Der Standardwert istForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True gibt an, dass der alte Wert ein eigenständiges Wort sein muss. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob Text in Löschrevisionen ignoriert werden soll. Der Standardwert ist`FALSCH` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in Feldcodes ignoriert werden soll. Der Standardwert ist`FALSCH` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in Feldern ignoriert werden soll. Der Standardwert ist`FALSCH` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Fußnoten ignoriert werden sollen. Der Standardwert ist`FALSCH` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in Einfügungsrevisionen ignoriert werden soll. Der Standardwert ist`FALSCH` . |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob Formen innerhalb eines Textes ignoriert werden sollen. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob der Inhalt ignoriert werden soll[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) . Der Standardwert ist`FALSCH` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, dass der alte Such-/Ersetzungsalgorithmus verwendet wird. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | „True“ gibt einen Vergleich unter Berücksichtigung der Groß-/Kleinschreibung an, „false“ zeigt einen Vergleich ohne Berücksichtigung der Groß-/Kleinschreibung an. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | Die benutzerdefinierte Methode, die vor jedem Ersetzen aufgerufen wird. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob der Absatz break ersetzt werden darf, wenn kein nächster gleichgeordneter Absatz vorhanden ist. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True gibt an, dass eine Textsuche der Reihe nach von oben nach unten unter Berücksichtigung der Textfelder durchgeführt wird. Der Standardwert ist`FALSCH` . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Ruft einen booleschen Wert ab, der angibt, ob Ersetzungen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen, oder legt diesen fest. Der Standardwert ist`FALSCH` . |

## Beispiele

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

Zeigt, wie eigenständige Such- und Ersetzungsvorgänge nur für Wörter umgeschaltet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Wir können ein „FindReplaceOptions“-Objekt verwenden, um den Such- und Ersetzungsprozess zu ändern.
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
