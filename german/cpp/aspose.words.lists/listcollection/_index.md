---
title: "Aspose::Words::Lists::ListCollection Klasse"
linktitle: "ListCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListCollection Klasse. Speichert und verwaltet die Formatierung von Aufzählungs‑ und nummerierten Listen, die in einem Dokument verwendet werden. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.lists/listcollection/
---
## ListCollection class


Speichert und verwaltet die Formatierung von Aufzählungs‑ und nummerierten Listen, die in einem Dokument verwendet werden. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(Aspose::Words::Lists::ListTemplate) | Erstellt eine neue Liste basierend auf einer vordefinierten Vorlage und fügt sie der Listensammlung im Dokument hinzu. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Erstellt eine neue Liste, die einen Listenvorlage‑Stil referenziert, und fügt sie der Listensammlung im Dokument hinzu. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Erstellt eine neue Liste, indem die angegebene Liste kopiert wird, und fügt sie der Listensammlung im Dokument hinzu. |
| [AddSingleLevelList](./addsinglelevellist/)(Aspose::Words::Lists::ListTemplate) | Erstellt eine neue einstufige Liste basierend auf der vordefinierten Vorlage und fügt sie der Listensammlung im Dokument hinzu. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Ermittelt die Anzahl nummerierter und Aufzählungslisten im Dokument. |
| [get_Document](./get_document/)() const | Ermittelt das übergeordnete Dokument. |
| [GetEnumerator](./getenumerator/)() override | Ermittelt das Enumerator-Objekt, das die Listen im Dokument aufzählt. |
| [GetListByListId](./getlistbylistid/)(int32_t) | Ermittelt eine Liste anhand einer Listenkennung. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ermittelt eine Liste anhand des Index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beschreibung |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Hinweise


Eine Liste in einem Microsoft‑Word‑Dokument ist ein Satz von Listformatierungseigenschaften. Die Formatierung der Listen wird in der [ListCollection](./)-Sammlung getrennt von den Textabsätzen gespeichert.

Sie erstellen keine Objekte dieser Klasse. Pro Dokument gibt es stets nur ein [ListCollection](./)-Objekt, das über die [Lists](../../aspose.words/documentbase/get_lists/)-Eigenschaft zugänglich ist.

Um eine neue Liste basierend auf einer vordefinierten Listenvorlage oder einem Listenstil zu erstellen, verwenden Sie die Methode [Add()](../).

Um eine neue Liste mit einer Formatierung zu erstellen, die einer bestehenden Liste identisch ist, verwenden Sie die Methode [AddCopy()](../).

Um einen Absatz als Aufzählungs‑ oder Nummerierungsabsatz zu formatieren, müssen Sie die Listformatierung auf den Absatz anwenden, indem Sie ein [List](../list/)-Objekt der [List](../listformat/get_list/)-Eigenschaft von [ListFormat](../listformat/) zuweisen.

Um die Listformatierung von einem Absatz zu entfernen, verwenden Sie die Methode [RemoveNumbers](../listformat/removenumbers/).

Wenn Sie ein wenig über WordprocessingML wissen, dann wissen Sie vielleicht, dass es separate Konzepte für „list“ und „list definition“ definiert. Das entspricht genau der Art und Weise, wie Listformatierungen auf niedriger Ebene in einem Microsoft‑Word‑Dokument gespeichert werden. Die [List](../list/)-Definition ist wie ein „Schema“ und die Liste ist wie eine Instanz einer Listendefinition.

Um das Programmiermodell zu vereinfachen, verbirgt Aspose.Words die Unterscheidung zwischen Liste und Listendefinition in ähnlicher Weise, wie Microsoft Word dies in seiner Benutzeroberfläche verbirgt. Dadurch können Sie sich mehr darauf konzentrieren, wie Ihr Dokument aussehen soll, anstatt Low‑Level‑Objekte zu erstellen, um die Anforderungen des Microsoft‑Word‑Dateiformats zu erfüllen.

In der aktuellen Version von [Aspose.Words](../../aspose.words/) ist es nicht möglich, Listen zu löschen, sobald sie erstellt wurden. Das ist ähnlich wie bei Microsoft Word, wo der Benutzer keine explizite Kontrolle über Listendefinitionen hat.

## Beispiele



Zeigt, wie man mit Listenebenen arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Eine Liste ermöglicht es uns, Absatzgruppen mit Präfixsymbolen und Einzügen zu organisieren und zu formatieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste einfügen, wird zu einem Element in der Liste.
// Unten sind zwei Listentypen, die wir mit einem Dokumenten‑Builder erstellen können.
// 1 -  Eine nummerierte Liste:
// Nummerierte Listen erzeugen eine logische Reihenfolge für ihre Absätze, indem sie jedes Element nummerieren.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// Durch das Setzen der Eigenschaft "ListLevelNumber" können wir die Listentiefe erhöhen
// um eine eigenständige Unterliste beim aktuellen Listenelement zu beginnen.
// Die Microsoft‑Word-Listenvorlage mit dem Namen "NumberDefault" verwendet Zahlen, um Listenniveaus für das erste Listenniveau zu erstellen.
// Tiefere Listenniveaus verwenden Buchstaben und kleine römische Ziffern.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Eine Aufzählungsliste:
// Diese Liste fügt vor jedem Absatz einen Einzug und ein Aufzählungszeichen ("•") ein.
// Tiefere Ebenen dieser Liste verwenden unterschiedliche Symbole, wie "■" und "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Wir können die Listformatierung deaktivieren, um nachfolgende Absätze nicht als Listen zu formatieren, indem wir das "List"‑Flag zurücksetzen.
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


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

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
