---
title: "Aspose::Words::Hyphenation::UnregisterDictionary method"
linktitle: "UnregisterDictionary"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Hyphenation::UnregisterDictionary method. Meldet ein Trennungswörterbuch für die angegebene Sprache ab. Dies unterscheidet sich vom Registrieren eines Null‑Wörterbuchs. Das Abmelden eines Wörterbuchs aktiviert den Callback für die angegebene Sprache in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation::UnregisterDictionary method


Meldet ein Silbentrennungswörterbuch für die angegebene Sprache ab. Dies unterscheidet sich vom Registrieren eines Null-Wörterbuchs. Das Abmelden eines Wörterbuchs aktiviert den Callback für die angegebene Sprache.

```cpp
static void Aspose::Words::Hyphenation::UnregisterDictionary(const System::String &language)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Sprache | const System::String\& | Ein Sprachname, z. B. "en-US". Siehe .NET-Dokumentation für "culture name" und RFC 4646 für Details. Wenn **null** oder ein leerer String, werden alle Wörterbücher abgemeldet. |

## Beispiele



Zeigt, wie man ein Trennungswörterbuch registriert.
```cpp
// Ein Trennungswörterbuch enthält eine Liste von Zeichenketten, die Trennungsregeln für die Sprache des Wörterbuchs definieren.
// Wenn ein Dokument Zeilen Text enthält, in denen ein Wort getrennt und in der nächsten Zeile fortgesetzt werden könnte,
// wird die Trennung die Liste von Zeichenketten des Wörterbuchs nach Teilzeichenketten dieses Wortes durchsuchen.
// Wenn das Wörterbuch eine Teilzeichenkette enthält, wird die Trennung das Wort über zwei Zeilen aufteilen
// an der Teilzeichenkette und einen Bindestrich an die erste Hälfte hinzufügen.
// Registrieren Sie eine Wörterbuchdatei vom lokalen Dateisystem für die Locale "de-CH".
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Öffnen Sie ein Dokument, das Text mit einer Locale enthält, die der unseres Wörterbuchs entspricht,
// und speichern Sie es in einem Festseiten‑Speicherformat. Der Text in diesem Dokument wird getrennt.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Run> >()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Run>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Run> r)>>([](System::SharedPtr<Aspose::Words::Run> r) -> bool
{
    return r->get_Font()->get_LocaleId() == System::MakeObject<System::Globalization::CultureInfo>(u"de-CH")->get_LCID();
}))));

doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Registered.pdf");

// Laden Sie das Dokument erneut, nachdem das Wörterbuch abgemeldet wurde,
// und speichern Sie es in ein weiteres PDF, das keinen getrennten Text enthält.
Aspose::Words::Hyphenation::UnregisterDictionary(u"de-CH");

ASSERT_FALSE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");
doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Unregistered.pdf");
```

## Siehe auch

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
