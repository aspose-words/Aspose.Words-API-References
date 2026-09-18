---
title: "Aspose::Words::Lists::ListLevel::get_NumberFormat Methode"
linktitle: "get_NumberFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListLevel::get_NumberFormat Methode. Gibt das Zahlenformat zurück oder legt es für die Listenebene in C++ fest."
type: docs
weight: 12000
url: /de/cpp/aspose.words.lists/listlevel/get_numberformat/
---
## ListLevel::get_NumberFormat method


Liefert oder setzt das Zahlenformat für die Listenebene.

```cpp
System::String Aspose::Words::Lists::ListLevel::get_NumberFormat() const
```

## Hinweise


Unter den normalen Textzeichen kann die Zeichenkette Platzhalterzeichen \x0000 bis \x0008 enthalten, die die Zahlen der entsprechenden Listenebenen darstellen.

Zum Beispiel erzeugt die Zeichenkette "\x0000.\x0001)" ein Listenelement, das etwa so aussieht: "1.5)". Die Zahl "1" ist die aktuelle Nummer der ersten Listenebene, die Zahl "5" ist die aktuelle Nummer der zweiten Listenebene.

Null ist nicht erlaubt, aber eine leere Zeichenkette, die keine Nummer bedeutet, ist gültig.

## Beispiele



Zeigt, wie benutzerdefinierte Listformatierung auf Absätze angewendet wird, wenn [DocumentBuilder](../../../aspose.words/documentbuilder/) verwendet wird.
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


Zeigt fortgeschrittene Methoden zur Anpassung von Listenelement‑Beschriftungen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Eine Liste ermöglicht es uns, Absatzgruppen mit Präfixsymbolen und Einzügen zu organisieren und zu formatieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste einfügen, wird zu einem Element in der Liste.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// Level‑1‑Beschriftungen werden gemäß dem Absatzstil "Heading 1" formatiert und erhalten ein Präfix.
// Diese sehen aus wie "Appendix A", "Appendix B"...
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"Appendix \x0000");
list->get_ListLevels()->idx_get(0)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);
list->get_ListLevels()->idx_get(0)->set_LinkedStyle(doc->get_Styles()->idx_get(u"Heading 1"));

// Level‑2‑Beschriftungen zeigen die aktuellen Nummern der ersten und zweiten Listenebene an und besitzen führende Nullen.
// Wenn die erste Listenebene bei 1 liegt, sehen die Listenelement‑Beschriftungen etwa so aus: "Section (1.01)", "Section (1.02)"...
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"Section (\x0000" u".\x0001" u")");
list->get_ListLevels()->idx_get(1)->set_NumberStyle(Aspose::Words::NumberStyle::LeadingZero);

// Beachte, dass die höhere Ebene die UppercaseLetter‑Nummerierung verwendet.
// Wir können die Eigenschaft "IsLegal" setzen, um arabische Zahlen für die höheren Listenebenen zu verwenden.
list->get_ListLevels()->idx_get(1)->set_IsLegal(true);
list->get_ListLevels()->idx_get(1)->set_RestartAfterLevel(0);

// Level‑3‑Beschriftungen werden in Großbuchstaben römische Zahlen mit einem Präfix und einem Suffix sein und bei jedem Listeneintrag der Ebene 1 neu beginnen.
// Diese Listenelement‑Beschriftungen sehen aus wie "-I-", "-II-"...
list->get_ListLevels()->idx_get(2)->set_NumberFormat(u"-\x0002" u"-");
list->get_ListLevels()->idx_get(2)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
list->get_ListLevels()->idx_get(2)->set_RestartAfterLevel(1);

// Mache die Beschriftungen aller Listenebenen fett.
for (auto&& level : list->get_ListLevels())
{
    level->get_Font()->set_Bold(true);
}

// Wende Listformatierung auf den aktuellen Absatz an.
builder->get_ListFormat()->set_List(list);

// Erstelle Listenelemente, die alle drei unserer Listenebenen anzeigen.
for (int32_t n = 0; n < 2; n++)
{
    for (int32_t i = 0; i < 3; i++)
    {
        builder->get_ListFormat()->set_ListLevelNumber(i);
        builder->Writeln(System::String(u"Level ") + i);
    }
}

builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.CreateListRestartAfterHigher.docx");
```

## Siehe auch

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
