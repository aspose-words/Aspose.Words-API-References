---
title: "Aspose::Words::Lists::ListLevel::get_IsLegal-Methode"
linktitle: "get_IsLegal"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListLevel::get_IsLegal-Methode. Wahr, wenn die Ebene alle vererbten Zahlen in Arabisch umwandelt, falsch, wenn sie deren Zahlenstil in C++ beibehält."
type: docs
weight: 10000
url: /de/cpp/aspose.words.lists/listlevel/get_islegal/
---
## ListLevel::get_IsLegal method


True, wenn die Ebene alle vererbten Zahlen in Arabisch umwandelt, false, wenn sie ihren Zahlenstil beibehält.

```cpp
bool Aspose::Words::Lists::ListLevel::get_IsLegal() const
```


## Beispiele



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
