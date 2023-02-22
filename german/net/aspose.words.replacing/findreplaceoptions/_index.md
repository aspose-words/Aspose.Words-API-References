---
title: Class FindReplaceOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Replacing.FindReplaceOptions klas. Gibt Optionen für Suchen/ErsetzenVorgänge an.
type: docs
weight: 4360
url: /de/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Gibt Optionen für Suchen/Ersetzen-Vorgänge an.

```csharp
public class FindReplaceOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Default_Constructor |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(FindReplaceDirection) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(IReplacingCallback) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(FindReplaceDirection, IReplacingCallback) |  |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Textformatierung auf neuen Inhalt angewendet. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Absatzformatierung auf neuen Inhalt angewendet. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Wählt die Richtung zum Ersetzen aus. Standardwert istForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True zeigt an, dass oldValue ein eigenständiges Wort sein muss. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text innerhalb von Löschrevisionen ignoriert werden soll. Der Standardwert ist`FALSCH` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in Feldcodes ignoriert werden soll. Der Standardwert ist`FALSCH` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text in Feldern ignoriert werden soll. Der Standardwert ist`FALSCH` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Fußnoten ignoriert werden sollen. Der Standardwert ist`FALSCH` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Text innerhalb von Einfügungsrevisionen ignoriert werden soll. Der Standardwert ist`FALSCH` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, dass der alte Suchen/Ersetzen-Algorithmus verwendet wird. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | „True“ gibt die Groß-/Kleinschreibung an, „false“ gibt die Groß- und Kleinschreibung an. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | Die benutzerdefinierte Methode, die vor jedem Ersetzen aufgerufen wird. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob Absatz break ersetzt werden darf, wenn kein nächster gleichgeordneter Absatz vorhanden ist. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True gibt an, dass eine Textsuche sequentiell von oben nach unten unter Berücksichtigung der Textfelder durchgeführt wird. Der Standardwert ist false. |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob Ersetzungen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen. Der Standardwert ist`FALSCH` . |

### Beispiele

Zeigt, wie die Groß-/Kleinschreibung beim Ausführen eines Suchen-und-Ersetzen-Vorgangs umgeschaltet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Wir können ein "FindReplaceOptions"-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das "MatchCase"-Flag auf "true", um die Groß-/Kleinschreibung beim Suchen von zu ersetzenden Zeichenfolgen anzuwenden.
// Setzen Sie das "MatchCase"-Flag auf "false", um die Groß-/Kleinschreibung bei der Suche nach zu ersetzendem Text zu ignorieren.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Zeigt, wie Sie eigenständige Suchen-und-Ersetzen-Operationen nur für Wörter umschalten können.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Wir können ein "FindReplaceOptions"-Objekt verwenden, um den Suchen-und-Ersetzen-Prozess zu ändern.
FindReplaceOptions options = new FindReplaceOptions();

// Setzen Sie das Flag "FindWholeWordsOnly" auf "true", um den gefundenen Text zu ersetzen, wenn er nicht Teil eines anderen Worts ist.
// Setzen Sie das Flag "FindWholeWordsOnly" auf "false", um den gesamten Text unabhängig von seiner Umgebung zu ersetzen.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Siehe auch

* namensraum [Aspose.Words.Replacing](../../aspose.words.replacing/)
* Montage [Aspose.Words](../../)


