---
title: "Aspose::Words::StyleCollection::Add method"
linktitle: "Add"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::StyleCollection::Add-Methode. Erstellt einen neuen benutzerdefinierten Stil und fügt ihn der Sammlung in C++ hinzu."
type: docs
weight: 2000
url: /de/cpp/aspose.words/stylecollection/add/
---
## StyleCollection::Add method


Erstellt einen neuen benutzerdefinierten Stil und fügt ihn der Sammlung hinzu.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::Add(Aspose::Words::StyleType type, const System::String &name)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| type | Aspose::Words::StyleType | Ein [StyleType](../../styletype/)-Wert, der den zu erstellenden Stiltyp angibt. |
| name | const System::String\& | Groß-/Kleinschreibung beachtender Name des zu erstellenden Stils. |
## Hinweise


Sie können Zeichen-, Absatz- oder Liststil erstellen.

Beim Erstellen eines Liststils wird der Stil mit der standardmäßigen nummerierten Listformatierung (1 \\ a \\ i) erstellt.

Wirft eine Ausnahme, wenn bereits ein Stil mit diesem Namen existiert.

## Beispiele



Zeigt, wie man einen List‑Stil erstellt und in einem Dokument verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Eine Liste ermöglicht es uns, Absatzgruppen mit Präfixsymbolen und Einzügen zu organisieren und zu formatieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste einfügen, wird zu einem Element in der Liste.
// Wir können ein komplettes List‑Objekt innerhalb eines Stils enthalten.
System::SharedPtr<Aspose::Words::Style> listStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle");

System::SharedPtr<Aspose::Words::Lists::List> list1 = listStyle->get_List();

ASSERT_TRUE(list1->get_IsListStyleDefinition());
ASSERT_FALSE(list1->get_IsListStyleReference());
ASSERT_TRUE(list1->get_IsMultiLevel());
ASPOSE_ASSERT_EQ(listStyle, list1->get_Style());

// Ändern Sie das Aussehen aller Listenebenen in unserer Liste.
for (auto&& level : list1->get_ListLevels())
{
    level->get_Font()->set_Name(u"Verdana");
    level->get_Font()->set_Color(System::Drawing::Color::get_Blue());
    level->get_Font()->set_Bold(true);
}

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Using list style first time:");

// Erstellen Sie eine weitere Liste aus einer Liste innerhalb eines Stils.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->Add(listStyle);

ASSERT_FALSE(list2->get_IsListStyleDefinition());
ASSERT_TRUE(list2->get_IsListStyleReference());
ASPOSE_ASSERT_EQ(listStyle, list2->get_Style());

// Fügen Sie einige Listenelemente hinzu, die unsere Liste formatieren wird.
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->Writeln(u"Using list style second time:");

// Erstellen und wenden Sie eine weitere Liste basierend auf dem Listenstil an.
System::SharedPtr<Aspose::Words::Lists::List> list3 = doc->get_Lists()->Add(listStyle);
builder->get_ListFormat()->set_List(list3);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateAndUseListStyle.docx");
```


Zeigt, wie ein [Style](../../style/) zur Stilsammlung eines Dokuments hinzugefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Legen Sie Standardparameter für neue Stile fest, die wir später zu dieser Sammlung hinzufügen können.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Wenn wir einen Stil vom Typ \"StyleType.Paragraph\" hinzufügen, wendet die Sammlung die Werte von
// seiner \"DefaultParagraphFormat\"-Eigenschaft auf die \"ParagraphFormat\"-Eigenschaft des Stils an.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Fügen Sie einen Stil hinzu und überprüfen Sie anschließend, ob er die Standardeinstellungen hat.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Siehe auch

* Class [Style](../../style/)
* Enum [StyleType](../../styletype/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
