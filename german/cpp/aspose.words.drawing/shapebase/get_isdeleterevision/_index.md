---
title: "Aspose::Words::Drawing::ShapeBase::get_IsDeleteRevision Methode"
linktitle: "get_IsDeleteRevision"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_IsDeleteRevision Methode. Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war, in C++."
type: docs
weight: 26000
url: /de/cpp/aspose.words.drawing/shapebase/get_isdeleterevision/
---
## ShapeBase::get_IsDeleteRevision method


Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDeleteRevision()
```


## Beispiele



Zeigt, wie man mit Revisionsformen arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_TrackRevisions());

// Füge eine Inline-Form ohne Verfolgung von Revisionen ein, wodurch diese Form keine Revision irgendeiner Art ist.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Beginnen Sie, Revisionen zu verfolgen, und fügen Sie dann eine weitere Form ein, die eine Revision sein wird.
doc->StartTrackRevisions(u"John Doe");

shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Sun);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

shapes[0]->Remove();

// Da wir diese Form entfernt haben, während wir Änderungen nachverfolgten,
// bleibt die Form im Dokument erhalten und wird als Löschrevision gezählt.
// Das Akzeptieren dieser Revision entfernt die Form dauerhaft, und das Ablehnen lässt sie im Dokument erhalten.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Cube, shapes[0]->get_ShapeType());
ASSERT_TRUE(shapes[0]->get_IsDeleteRevision());

// Und wir haben eine weitere Form eingefügt, während wir Änderungen nachverfolgten, sodass diese Form als Einfüge‑Revision gezählt wird.
// Das Akzeptieren dieser Revision wird diese Form als Nicht‑Revision in das Dokument integrieren,
// und das Ablehnen der Revision wird diese Form dauerhaft entfernen.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Sun, shapes[1]->get_ShapeType());
ASSERT_TRUE(shapes[1]->get_IsInsertRevision());
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
