---
title: "Aspose::Words::Lists::ListCollection::AddCopy Methode"
linktitle: "AddCopy"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListCollection::AddCopy Methode. Erstellt eine neue Liste, indem die angegebene Liste kopiert und zur Sammlung von Listen im Dokument in C++ hinzugefügt wird."
type: docs
weight: 3000
url: /de/cpp/aspose.words.lists/listcollection/addcopy/
---
## ListCollection::AddCopy method


Erstellt eine neue Liste, indem die angegebene Liste kopiert wird, und fügt sie der Listensammlung im Dokument hinzu.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddCopy(const System::SharedPtr<Aspose::Words::Lists::List> &srcList)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcList | const System::SharedPtr\<Aspose::Words::Lists::List\>\& | Die Quellliste, von der kopiert werden soll. |

### ReturnValue

Die neu erstellte Liste.
## Hinweise


Die Quellliste kann aus einem beliebigen Dokument stammen. Wenn die Quellliste zu einem anderen Dokument gehört, wird eine Kopie der Liste erstellt und dem aktuellen Dokument hinzugefügt.

Wenn die Quellliste eine Referenz oder Definition eines Listenstils ist, ist die neu erstellte Liste nicht mit dem ursprünglichen Listenstil verbunden.

## Beispiele



Zeigt, wie man die Nummerierung in einer Liste durch Kopieren einer Liste neu startet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Eine Liste ermöglicht es uns, Absatzgruppen mit Präfixsymbolen und Einzügen zu organisieren und zu formatieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste einfügen, wird zu einem Element in der Liste.
// Erstellen Sie eine Liste aus einer Microsoft‑Word-Vorlage und passen Sie ihr erstes Listenniveau an.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Wenden Sie unsere Liste auf einige Absätze an.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Wir können eine Kopie einer bestehenden Liste zur Listensammlung des Dokuments hinzufügen
// um eine ähnliche Liste zu erstellen, ohne das Original zu ändern.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Wenden Sie die zweite Liste auf neue Absätze an.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## Siehe auch

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
