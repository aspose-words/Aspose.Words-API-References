---
title: "Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision Methode"
linktitle: "get_IsMoveToRevision"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision Methode. Gibt true zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung in C++ aktiviert war."
type: docs
weight: 34000
url: /de/cpp/aspose.words.drawing/shapebase/get_ismovetorevision/
---
## ShapeBase::get_IsMoveToRevision method


Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsMoveToRevision()
```


## Beispiele



Zeigt, wie man Formen von Verschiebungsrevisionen identifiziert.
```cpp
// Eine Verschiebungsrevision liegt vor, wenn wir ein Element im Dokumentkörper durch Ausschneiden und Einfügen in Microsoft Word verschieben, während
// die Änderungen nachverfolgt werden. Wenn wir eine Inline-Form in eine solche Textbewegung einbeziehen, wird diese Form ebenfalls zu einer Revision.
// Kopieren-und-Einfügen oder Verschieben von schwebenden Formen erzeugen keine Verschiebungsrevisionen.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision shape.docx");

// Verschiebungsrevisionen bestehen aus Paaren von "Move from"- und "Move to"-Revisionen. Wir haben in diesem Dokument eine Form verschoben,
// aber bis wir die Verschiebungsrevision akzeptieren oder ablehnen, wird es zwei Instanzen dieser Form geben.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

// Dies ist die \"Move to\"-Revision, die die Form an ihrem Ankunftsziel ist.
// Wenn wir die Revision akzeptieren, wird diese \"Move to\"-Revisionsform verschwinden,
// und die \"Move from\"-Revisionsform bleibt erhalten.
ASSERT_FALSE(shapes[0]->get_IsMoveFromRevision());
ASSERT_TRUE(shapes[0]->get_IsMoveToRevision());

// Dies ist die \"Move from\"-Revision, die die Form an ihrem ursprünglichen Ort ist.
// Wenn wir die Revision akzeptieren, wird diese \"Move from\"-Revisionsform verschwinden,
// und die \"Move to\"-Revisionsform bleibt erhalten.
ASSERT_TRUE(shapes[1]->get_IsMoveFromRevision());
ASSERT_FALSE(shapes[1]->get_IsMoveToRevision());
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
