---
title: "Aspose::Words::Hyphenation::RegisterDictionary method"
linktitle: "RegisterDictionary"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Hyphenation::RegisterDictionary method. Registriert und lädt ein Trennungswörterbuch für die angegebene Sprache aus einem Stream. Wirft eine Ausnahme, wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/hyphenation/registerdictionary/
---
## Hyphenation::RegisterDictionary(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Registriert und lädt ein Silbentrennungs‑Wörterbuch für die angegebene Sprache aus einem Stream. Wirft eine Ausnahme, wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Sprache | const System::String\& | Ein Sprachname, z. B. "en-US". Siehe .NET-Dokumentation für "culture name" und RFC 4646 für Details. |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Ein Stream für die Wörterbuchdatei im OpenOffice-Format. |

## Siehe auch

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Hyphenation::RegisterDictionary(const System::String\&, const System::String\&) method


Registriert und lädt ein Silbentrennungswörterbuch für die angegebene Sprache aus einer Datei. Wirft eine Ausnahme, wenn das Wörterbuch nicht gelesen werden kann oder ein ungültiges Format hat. Diese Methode kann auch verwendet werden, um ein Null‑Wörterbuch zu registrieren, um zu verhindern, dass [Callback](../get_callback/) wiederholt für dieselbe Sprache aufgerufen wird.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::String &fileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Sprache | const System::String\& | Ein Sprachname, z. B. "en-US". Siehe .NET-Dokumentation für "culture name" und RFC 4646 für Details. |
| fileName | const System::String\& | Ein Pfad zur Wörterbuchdatei im Open‑Office‑Format. Wenn dieser Parameter **null** oder ein leerer String ist, wird ein Null‑Wörterbuch registriert und der Callback wird für diese Sprache nicht mehr aufgerufen. Um den Callback wieder zu aktivieren, verwenden Sie die Methode [UnregisterDictionary()](../). |

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
## Hyphenation::RegisterDictionary(System::String, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::Hyphenation::RegisterDictionary(System::String language, std::basic_istream<CharType, Traits> &stream)
```

## Siehe auch

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
