---
title: "Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision method"
linktitle: "get_IsMoveToRevision"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision method. Returnerar true om detta objekt flyttades (infogades) i Microsoft Word medan spårning av ändringar var aktiverad i C++."
type: docs
weight: 34000
url: /sv/cpp/aspose.words.drawing/shapebase/get_ismovetorevision/
---
## ShapeBase::get_IsMoveToRevision method


Returnerar **true** om detta objekt flyttades (infogades) i Microsoft Word medan spårning av ändringar var aktiverad.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision()
```


## Exempel



Visar hur man identifierar flyttrevisionsformer.
```cpp
// En flyttrevision är när vi flyttar ett element i dokumentkroppen genom att klippa och klistra in det i Microsoft Word medan
// spårar ändringar. Om vi involverar en inline-form i en sådan textförflyttning, blir den formen också en revision.
// Kopiering och inklistring eller flyttning av flytande former skapar inte flyttrevisioner.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision shape.docx");

// Flyttrevisioner består av par av "Move from"- och "Move to"-revisioner. Vi flyttade i detta dokument i en form,
// men tills vi accepterar eller avvisar flyttrevisionen, kommer det att finnas två instanser av den formen.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// Detta är "Move to"-revisionen, som är formen vid dess ankomstdestination.
// Om vi accepterar revisionen, kommer denna "Move to"-revisionsform att försvinna,
// och den "Move from"-revisionsformen kommer att kvarstå.
ASSERT_FALSE(shapes[0]->get_IsMoveFromRevision());
ASSERT_TRUE(shapes[0]->get_IsMoveToRevision());

// Detta är "Move from"-revisionen, som är formen på dess ursprungliga plats.
// Om vi accepterar revisionen, kommer denna "Move from"-revisionsform att försvinna,
// och den "Move to"-revisionsformen kommer att kvarstå.
ASSERT_TRUE(shapes[1]->get_IsMoveFromRevision());
ASSERT_FALSE(shapes[1]->get_IsMoveToRevision());
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
