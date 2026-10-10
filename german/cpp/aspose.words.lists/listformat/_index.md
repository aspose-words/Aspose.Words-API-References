---
title: "Aspose::Words::Lists::ListFormat Klasse"
linktitle: "ListFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListFormat Klasse. Ermöglicht die Steuerung, welche Listformatierung auf einen Absatz angewendet wird. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.lists/listformat/
---
## ListFormat class


Ermöglicht die Steuerung, welche Listenformatierung auf einen Absatz angewendet wird. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListFormat : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ApplyBulletDefault](./applybulletdefault/)() | Startet eine neue Standard-Aufzählungsliste und wendet sie auf den Absatz an. |
| [ApplyNumberDefault](./applynumberdefault/)() | Startet eine neue Standard-Nummerierungsliste und wendet sie auf den Absatz an. |
| [get_IsListItem](./get_islistitem/)() | Wahr, wenn auf den Absatz eine Aufzählungs- oder Nummerierungsformatierung angewendet wurde. |
| [get_List](./get_list/)() | Liest oder setzt die Liste, zu der dieser Absatz gehört. |
| [get_ListLevel](./get_listlevel/)() | Gibt die Listenebenenformatierung plus etwaige Formatierungsüberschreibungen zurück, die auf den aktuellen Absatz angewendet wurden. |
| [get_ListLevelNumber](./get_listlevelnumber/)() | Liest oder setzt die Listenebenennummer (0 bis 8) für den Absatz. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ListIndent](./listindent/)() | Erhöht die Listenebene des aktuellen Absatzes um eine Ebene. |
| [ListOutdent](./listoutdent/)() | Verringert die Listenebene des aktuellen Absatzes um eine Ebene. |
| [RemoveNumbers](./removenumbers/)() | Entfernt Zahlen oder Aufzählungszeichen aus dem aktuellen Absatz und setzt die Listenebene auf Null. |
| [set_List](./set_list/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Setter für [Aspose::Words::Lists::ListFormat::get_List](./get_list/). |
| [set_ListLevelNumber](./set_listlevelnumber/)(int32_t) | Setter für [Aspose::Words::Lists::ListFormat::get_ListLevelNumber](./get_listlevelnumber/). |
| static [Type](./type/)() |  |
## Hinweise


Ein Absatz in einem Microsoft‑Word‑Dokument kann Aufzählungszeichen oder Nummern enthalten. Wenn ein Absatz Aufzählungszeichen oder Nummern enthält, sagt man, dass eine Listformatierung auf den Absatz angewendet wurde.

Sie erstellen Objekte der Klasse [ListFormat](./) nicht direkt. Sie greifen auf [ListFormat](./) als Eigenschaft eines anderen Objekts zu, das eine Listformatierung besitzen kann. Derzeit sind dies die Objekte: [Paragraph](../../aspose.words/paragraph/), [Style](../../aspose.words/style/) und [DocumentBuilder](../../aspose.words/documentbuilder/).

[ListFormat](./) of a [Paragraph](../../aspose.words/paragraph/) specifies what list formatting and list level is applied to that particular paragraph.

[ListFormat](./) of a [Style](../../aspose.words/style/) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

[ListFormat](./) of a [DocumentBuilder](../../aspose.words/documentbuilder/) provides access to the list formatting at the current cursor position inside the [DocumentBuilder](../../aspose.words/documentbuilder/).

Die Listformatierung selbst wird in einem [List](../list/)‑Objekt gespeichert, das getrennt von den Absätzen liegt. Die List‑Objekte werden in einer [ListCollection](../listcollection/)‑Sammlung abgelegt. Pro [Document](../../aspose.words/document/) gibt es genau eine [ListCollection](../listcollection/)‑Sammlung.

Die Absätze gehören nicht physisch zu einer Liste. Die Absätze verweisen lediglich über die Eigenschaft [List](./get_list/) auf ein bestimmtes List‑Objekt und über die Eigenschaft [ListLevelNumber](./get_listlevelnumber/) auf eine bestimmte Ebene in der Liste. Durch das Setzen dieser beiden Eigenschaften steuern Sie, welche Aufzählungszeichen und Nummerierung auf einen Absatz angewendet werden.

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

## Siehe auch

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
