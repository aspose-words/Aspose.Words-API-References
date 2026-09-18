---
title: "Aspose::Words::Replacing::FindReplaceOptions Klasse"
linktitle: "FindReplaceOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Replacing::FindReplaceOptions Klasse. Gibt Optionen für Such‑/Ersetzungs‑Operationen an. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class


Gibt Optionen für Suchen/Ersetzen-Operationen an. Weitere Informationen finden Sie im [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/) Dokumentationsartikel.

```cpp
class FindReplaceOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [FindReplaceOptions](./findreplaceoptions/)() | Initialisiert eine neue Instanz der [FindReplaceOptions](./) Klasse mit den Standardeinstellungen. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection) | Initialisiert eine neue Instanz der [FindReplaceOptions](./) Klasse mit der angegebenen Richtung. |
| [FindReplaceOptions](./findreplaceoptions/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Initialisiert eine neue Instanz der [FindReplaceOptions](./) Klasse mit dem angegebenen Ersetzungs‑Callback. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Initialisiert eine neue Instanz der [FindReplaceOptions](./) Klasse mit der angegebenen Richtung und dem Ersetzungs‑Callback. |
| [get_ApplyFont](./get_applyfont/)() const | Textformatierung, die auf neuen Inhalt angewendet wird. |
| [get_ApplyParagraphFormat](./get_applyparagraphformat/)() const | [Paragraph](../../aspose.words/paragraph/) Formatierung, die auf neuen Inhalt angewendet wird. |
| [get_Direction](./get_direction/)() const | Wählt die Richtung für das Ersetzen aus. Standardwert ist [Forward](../findreplacedirection/). |
| [get_FindWholeWordsOnly](./get_findwholewordsonly/)() const | True gibt an, dass oldValue ein eigenständiges Wort sein muss. |
| [get_IgnoreDeleted](./get_ignoredeleted/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob Text innerhalb von Löschrevisionen ignoriert werden soll. Der Standardwert ist **false**. |
| [get_IgnoreFieldCodes](./get_ignorefieldcodes/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob Text innerhalb von Feldcodes ignoriert werden soll. Der Standardwert ist **false**. |
| [get_IgnoreFields](./get_ignorefields/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob Text innerhalb von Feldern ignoriert werden soll. Der Standardwert ist **false**. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob Fußnoten ignoriert werden sollen. Der Standardwert ist **false**. |
| [get_IgnoreInserted](./get_ignoreinserted/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob Text innerhalb von Einfüge‑Revisionen ignoriert werden soll. Der Standardwert ist **false**. |
| [get_IgnoreOfficeMath](./get_ignoreofficemath/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob Text innerhalb von OfficeMath/> ignoriert werden soll. Der Standardwert ist **true**. |
| [get_IgnoreShapes](./get_ignoreshapes/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob Formen innerhalb eines Textes ignoriert werden sollen. Der Standardwert ist **false** |
| [get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob der Inhalt von [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) ignoriert werden soll. Der Standardwert ist **false**. |
| [get_LegacyMode](./get_legacymode/)() const | Liest oder setzt einen booleschen Wert, der angibt, dass der alte Such‑/Ersetzungsalgorithmus verwendet wird. |
| [get_MatchCase](./get_matchcase/)() const | True zeigt einen case‑sensitiven Vergleich an, false zeigt einen case‑insensitiven Vergleich an. |
| [get_ReplacementFormat](./get_replacementformat/)() const | Gibt das Format der Ersetzung an. Standard ist [Text](../replacementformat/). |
| [get_ReplacingCallback](./get_replacingcallback/)() const | Die benutzerdefinierte Methode, die vor jedem Ersetzungsereignis aufgerufen wird. |
| [get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob ein Absatzumbruch ersetzt werden darf, wenn kein nachfolgender Geschwisterabsatz vorhanden ist. Der Standardwert ist **false**. |
| [get_UseLegacyOrder](./get_uselegacyorder/)() const | True zeigt an, dass eine Textsuche sequenziell von oben nach unten unter Berücksichtigung von Textfeldern durchgeführt wird. Der Standardwert ist **false**. |
| [get_UseSubstitutions](./get_usesubstitutions/)() const | Liest oder setzt einen booleschen Wert, der angibt, ob Substitutionen innerhalb von Ersetzungsmustern erkannt und verwendet werden sollen. Der Standardwert ist **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Direction](./set_direction/)(Aspose::Words::Replacing::FindReplaceDirection) | Wählt die Richtung für das Ersetzen aus. Standardwert ist [Forward](../findreplacedirection/). |
| [set_FindWholeWordsOnly](./set_findwholewordsonly/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly](./get_findwholewordsonly/). |
| [set_IgnoreDeleted](./set_ignoredeleted/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted](./get_ignoredeleted/). |
| [set_IgnoreFieldCodes](./set_ignorefieldcodes/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes](./get_ignorefieldcodes/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreInserted](./set_ignoreinserted/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted](./get_ignoreinserted/). |
| [set_IgnoreOfficeMath](./set_ignoreofficemath/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath](./get_ignoreofficemath/). |
| [set_IgnoreShapes](./set_ignoreshapes/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes](./get_ignoreshapes/). |
| [set_IgnoreStructuredDocumentTags](./set_ignorestructureddocumenttags/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/). |
| [set_LegacyMode](./set_legacymode/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode](./get_legacymode/). |
| [set_MatchCase](./set_matchcase/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase](./get_matchcase/). |
| [set_ReplacementFormat](./set_replacementformat/)(Aspose::Words::Replacing::ReplacementFormat) | Gibt das Format der Ersetzung an. Standard ist [Text](../replacementformat/). |
| [set_ReplacingCallback](./set_replacingcallback/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Die benutzerdefinierte Methode, die vor jedem Ersetzungsereignis aufgerufen wird. |
| [set_SmartParagraphBreakReplacement](./set_smartparagraphbreakreplacement/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/). |
| [set_UseLegacyOrder](./set_uselegacyorder/)(bool) | True zeigt an, dass eine Textsuche sequenziell von oben nach unten unter Berücksichtigung von Textfeldern durchgeführt wird. Der Standardwert ist **false**. |
| [set_UseSubstitutions](./set_usesubstitutions/)(bool) | Setter für [Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions](./get_usesubstitutions/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie die Groß‑/Kleinschreibung bei einer Suchen‑und‑Ersetzen‑Operation umgeschaltet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Wir können ein "FindReplaceOptions"‑Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Setzen Sie das "MatchCase"‑Flag auf "true", um bei der Suche nach zu ersetzenden Zeichenketten die Groß‑/Kleinschreibung zu berücksichtigen.
// Setzen Sie das "MatchCase"‑Flag auf "false", um die Groß‑/Kleinschreibung bei der Suche nach zu ersetzendem Text zu ignorieren.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Zeigt, wie man eigenständige wort‑nur‑Suchen‑und‑Ersetzen‑Operationen umschaltet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Wir können ein "FindReplaceOptions"‑Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Setzen Sie das Flag "FindWholeWordsOnly" auf "true", um den gefundenen Text zu ersetzen, wenn er nicht Teil eines anderen Wortes ist.
// Setzen Sie das Flag "FindWholeWordsOnly" auf "false", um allen Text zu ersetzen, unabhängig von seiner Umgebung.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## Siehe auch

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
