---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision metod"
linktitle: "get_IsInsertRevision"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision metod. Returnerar **true** om detta objekt infogades i Microsoft Word medan spårning av ändringar var aktiverad i C++."
type: docs
weight: 31000
url: /sv/cpp/aspose.words.drawing/shapebase/get_isinsertrevision/
---
## ShapeBase::get_IsInsertRevision method


Returnerar true om detta objekt infogades i Microsoft Word medan spårning av ändringar var aktiverad.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInsertRevision()
```


## Exempel



Visar hur man arbetar med revisionsformer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_TrackRevisions());

// Infoga en inline-form utan att spåra revisioner, vilket gör att denna form inte blir någon revision alls.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Starta spårning av revisioner och infoga sedan en annan form, vilket blir en revision.
doc->StartTrackRevisions(u"John Doe");

shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Sun);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

shapes[0]->Remove();

// Eftersom vi tog bort den formen medan vi spårade ändringar,
// formen kvarstår i dokumentet och räknas som en raderingsrevision.
// Att acceptera denna revision kommer att ta bort formen permanent, och att avvisa den kommer att behålla den i dokumentet.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Cube, shapes[0]->get_ShapeType());
ASSERT_TRUE(shapes[0]->get_IsDeleteRevision());

// Och vi infogade en annan form medan vi spårade ändringar, så den formen kommer att räknas som en infogningsrevision.
// Att acceptera denna revision kommer att assimilera denna form i dokumentet som en icke-revision,
// och att avvisa revisionen kommer att ta bort den här formen permanent.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Sun, shapes[1]->get_ShapeType());
ASSERT_TRUE(shapes[1]->get_IsInsertRevision());
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
