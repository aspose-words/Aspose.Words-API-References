---
title: "Aspose::Words::Lists::ListLevelAlignment enum"
linktitle: "ListLevelAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListLevelAlignment enum. Gibt die Ausrichtung für die Listennummer oder das Aufzählungszeichen in C++ an."
type: docs
weight: 7000
url: /de/cpp/aspose.words.lists/listlevelalignment/
---
## ListLevelAlignment enum


Gibt die Ausrichtung für die Listennummer oder das Aufzählungszeichen an.

```cpp
enum class ListLevelAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Links | 0 | Das Listenelement ist links von der Nummerposition ausgerichtet. |
| Mitte | 1 | Das Listenelement ist an der Nummerposition zentriert. |
| Rechts | 2 | Dieses Listenelement ist rechts von der Nummerposition ausgerichtet. |

## Hinweise


Wird als Wert für die [Alignment](../listlevel/get_alignment/) Eigenschaft verwendet.

## Beispiele



Zeigt, wie benutzerdefinierte Listformatierung auf Absätze angewendet wird, wenn [DocumentBuilder](../../aspose.words/documentbuilder/) verwendet wird.
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

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
