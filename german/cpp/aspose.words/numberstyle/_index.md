---
title: "Aspose::Words::NumberStyle‑Enum"
linktitle: "NumberStyle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NumberStyle‑Enum. Gibt den Zahlenstil für eine Liste, Fußnoten und Endnoten sowie Seitenzahlen in C++ an."
type: docs
weight: 103000
url: /de/cpp/aspose.words/numberstyle/
---
## NumberStyle enum


Gibt den Zahlenstil für eine Liste, Fußnoten und Endnoten sowie Seitenzahlen an.

```cpp
enum class NumberStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Arabisch | 0 | Arabische Nummerierung (1, 2, 3, ...) |
| UppercaseRoman | 1 | Großbuchstaben-Römisch (I, II, III, ...) |
| LowercaseRoman | 2 | Kleinbuchstaben-Römisch (i, ii, iii, ...) |
| UppercaseLetter | 3 | Großbuchstaben (A, B, C, ...) |
| LowercaseLetter | 4 | Kleinbuchstaben (a, b, c, ...) |
| Ordinal | 5 | Ordinal (1., 2., 3., ...) |
| Number | 6 | Nummeriert (Eins, Zwei, Drei, ...) |
| OrdinalText | 7 | Ordinal (text) (Erste, Zweite, Dritte, ...) |
| Hex | 8 | Hexadezimal: 8, 9, A, B, C, D, E, F, 10, 11, 12. |
| ChicagoManual | 9 | Chicago-Handbuch für [Style](../style/): *, †, † |
| Kanji | 10 | Ideographisch-digital. |
| KanjiDigit | 11 | Japanische Zählung. |
| AiueoHalfWidth | 12 | Aiueo. |
| IrohaHalfWidth | 13 | Iroha. |
| ArabicFullWidth | 14 | Vollbreite Arabisch: 1, 2, 3, 4. |
| ArabicHalfWidth | 15 | Halbbreite Arabisch: 1, 2, 3, 4. |
| KanjiTraditional | 16 | Japanisch rechtlich. |
| KanjiTraditional2 | 17 | Japanisch digitale Zehntausend. |
| NumberInCircle | 18 | Eingeschlossene Kreise. |
| DecimalFullWidth | 19 | Dezimal volle Breite: 1, 2, 3, 4. |
| Aiueo | 20 | Aiueo volle Breite. |
| Iroha | 21 | Iroha volle Breite. |
| LeadingZero | 22 | Führende Null (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| Bullet | 23 | Bullet (prüfen Sie den Zeichencode im Text) |
| Ganada | 24 | Koreanisch Ganada. |
| Chosung | 25 | Korea Chosung. |
| GB1 | 26 | Eingeschlossener Punkt. |
| GB2 | 27 | Eingeschlossene Klammer. |
| GB3 | 28 | Eingeschlossener chinesischer Kreis. |
| GB4 | 29 | Ideogramm eingeschlossener Kreis. |
| Zodiac1 | 30 | Traditionelles Ideogramm. |
| Zodiac2 | 31 | Ideogramm Tierkreis. |
| Zodiac3 | 32 | Ideogramm Tierkreis traditionell. |
| TradChinNum1 | 33 | Taiwanesische Zählung. |
| TradChinNum2 | 34 | Ideogramm rechtlich traditionell. |
| TradChinNum3 | 35 | Taiwanesische Zählung Tausend. |
| TradChinNum4 | 36 | Taiwanesisch digital. |
| SimpChinNum1 | 37 | Chinesische Zählung. |
| SimpChinNum2 | 38 | Chinesisch rechtlich vereinfacht. |
| SimpChinNum3 | 39 | Chinesische Zählung Tausend. |
| SimpChinNum4 | 40 | Chinesisch (nicht implementiert) |
| HanjaRead | 41 | Koreanisch digital. |
| HanjaReadDigit | 42 | Koreanisch Zählen. |
| Hangul | 43 | Korea rechtlich. |
| Hanja | 44 | Korea digital2. |
| Hebrew1 | 45 | Hebräisch-1. |
| Arabic1 | 46 | Arabisch alpha. |
| Hebrew2 | 47 | Hebräisch-2. |
| Arabic2 | 48 | Arabisch abjad. |
| HindiLetter1 | 49 | Hindi-Vokale. |
| HindiLetter2 | 50 | Hindi-Konsonanten. |
| HindiArabic | 51 | Hindi-Zahlen. |
| HindiCardinalText | 52 | Hindi beschreibend (Kardinalzahlen) |
| ThaiLetter | 53 | Thai-Buchstaben. |
| ThaiArabic | 54 | Thai-Zahlen. |
| ThaiCardinalText | 55 | Thai beschreibend (Kardinalzahlen) |
| VietCardinalText | 56 | Vietnamesisch beschreibend (Kardinalzahlen) |
| NumberInDash | 57 | Seitenzahlenformat: - 1 -, - 2 -, - 3 -, - 4 -. |
| KleinbuchstabenRussisch | 58 | Kleinbuchstaben des russischen Alphabets. |
| GroßbuchstabenRussisch | 59 | Großbuchstaben des russischen Alphabets. |
| Keine | 255 | Keine Aufzählungszeichen oder Nummer. |
| Benutzerdefiniert | 65280 | Benutzerdefiniertes Zahlenformat. Es wird nur vom DOCX-Format unterstützt. |


## Beispiele



Zeigt, wie benutzerdefinierte Listformatierung auf Absätze angewendet wird, wenn [DocumentBuilder](../documentbuilder/) verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Eine Liste ermöglicht es uns, Absatzgruppen mit Präfixsymbolen und Einzügen zu organisieren und zu formatieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste einfügen, wird zu einem Element in der Liste.
// Erstellen Sie eine Liste aus einer Microsoft‑Word‑Vorlage und passen Sie die ersten beiden Ebenen der Liste an.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Dieser NumberFormat‑Wert erzeugt sternförmige Aufzählungszeichen.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Erstellen Sie Absätze und wenden Sie beide Listenebenen unserer benutzerdefinierten Listformatierung darauf an.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
