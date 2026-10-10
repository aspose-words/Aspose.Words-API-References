---
title: "Aspose::Words::Fields::FieldShape::get_Text Methode"
linktitle: "get_Text"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldShape::get_Text Methode. Liest oder setzt den Text, der in C++ abgerufen wird."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldshape/get_text/
---
## FieldShape::get_Text method


Ermittelt oder legt den abzurufenden Text fest.

```cpp
System::String Aspose::Words::Fields::FieldShape::get_Text()
```


## Beispiele



Zeigt, wie man rechts-nach-links-kompatible Listen mit BIDIOUTLINE-Feldern erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Das BIDIOUTLINE-Feld nummeriert Absätze wie die AUTONUM/LISTNUM-Felder,
// ist jedoch nur sichtbar, wenn eine rechts-nach-links Bearbeitungssprache aktiviert ist, wie Hebräisch oder Arabisch.
// Das folgende Feld zeigt ".1" an, das RTL-Äquivalent der Listennummer "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// Fügen Sie zwei weitere BIDIOUTLINE-Felder hinzu, die ".2" und ".3" anzeigen.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// Setzen Sie die horizontale Textausrichtung für jeden Absatz im Dokument auf RTL.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// Wenn wir in Microsoft Word eine rechts-nach-links Bearbeitungssprache aktivieren, zeigen unsere Felder Zahlen an.
// Andernfalls zeigen sie "###" an.
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


Zeigt, wie einige ältere Microsoft Word-Felder wie SHAPE und EMBED beim Laden verarbeitet werden.
```cpp
// Öffnen Sie ein Dokument, das in Microsoft Word 2003 erstellt wurde.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy fields.doc");

// Wenn wir das Word-Dokument öffnen und Alt+F9 drücken, sehen wir ein SHAPE- und ein EMBED-Feld.
// Ein SHAPE-Feld ist der Anker/Canvas für ein AutoShape-Objekt mit aktiviertem Umbruchstil "In Zeile mit Text".
// Ein EMBED-Feld hat dieselbe Funktion, jedoch für ein eingebettetes Objekt,
// wie eine Tabellenkalkulation aus einem externen Excel-Dokument.
// Allerdings werden diese Felder nicht in der Feldsammlung des Dokuments angezeigt.
ASSERT_EQ(0, doc->get_Range()->get_Fields()->get_Count());

// Diese Felder werden nur von alten Versionen von Microsoft Word unterstützt.
// Der Ladevorgang des Dokuments konvertiert diese Felder in Shape-Objekte,
// auf die wir in der Knotensammlung des Dokuments zugreifen können.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);
ASSERT_EQ(3, shapes->get_Count());

// Der erste Shape-Knoten entspricht dem SHAPE-Feld im Eingabedokument,
// das das Inline-Canvas für das AutoShape ist.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Image, shape->get_ShapeType());

// Der zweite Shape-Knoten ist das AutoShape selbst.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Can, shape->get_ShapeType());

// Der dritte Shape ist das frühere EMBED-Feld, das die externe Tabellenkalkulation enthielt.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(2));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::OleObject, shape->get_ShapeType());
```

## Siehe auch

* Class [FieldShape](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
