---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInline Methode"
linktitle: "get_IsInline"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInline Methode. Eine schnelle Möglichkeit, zu bestimmen, ob diese Form inline mit Text positioniert ist, in C++."
type: docs
weight: 30000
url: /de/cpp/aspose.words.drawing/shapebase/get_isinline/
---
## ShapeBase::get_IsInline method


Eine schnelle Möglichkeit zu bestimmen, ob diese Form im Textfluss positioniert ist.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInline()
```

## Hinweise


Wirkt nur bei Formen der obersten Ebene.

## Beispiele



Zeigt, wie man bestimmt, ob eine Form inline oder schwebend ist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Unten sind zwei Umbruchtypen aufgeführt, die Formen haben können.
// 1 -  Inline:
builder->Write(u"Hello world! ");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());
builder->Write(u" Hello again.");

// Eine Inline-Form befindet sich innerhalb eines Absatzes zusammen mit anderen Absatzelementen, wie Textläufen.
// In Microsoft Word können wir die Form anklicken und an jeden Absatz ziehen, als wäre sie ein Zeichen.
// Wenn die Form groß ist, wirkt sie sich auf den vertikalen Absatzabstand aus.
// Wir können diese Form nicht an einen Ort ohne Absatz verschieben.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::Inline, shape->get_WrapType());
ASSERT_TRUE(shape->get_IsInline());

// 2 -  Schwebend:
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

// Eine schwebende Form gehört zu dem Absatz, in den wir sie einfügen,
// was wir anhand eines Ankersymbols erkennen können, das erscheint, wenn wir die Form anklicken.
// Wenn die Form kein sichtbares Ankersymbol links von ihr hat,
// müssen wir sichtbare Anker über "Optionen" -> "Anzeige" -> "Objektanker" aktivieren.
// In Microsoft Word können wir mit der linken Maustaste klicken und diese Form frei an jede Position ziehen.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, shape->get_WrapType());
ASSERT_FALSE(shape->get_IsInline());

doc->Save(get_ArtifactsDir() + u"Shape.IsInline.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
