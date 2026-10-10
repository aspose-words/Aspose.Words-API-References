---
title: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked Methode"
linktitle: "get_AnchorLocked"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked Methode. Gibt an, ob der Anker der Form gesperrt ist in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.drawing/shapebase/get_anchorlocked/
---
## ShapeBase::get_AnchorLocked method


Gibt an, ob der Anker der Form gesperrt ist.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AnchorLocked()
```

## Hinweise


Der Standardwert ist **false**.

Wirkt nur bei Formen der obersten Ebene.

Diese Eigenschaft beeinflusst das Verhalten des Ankers der Form in Microsoft Word. Wenn der Anker nicht gesperrt ist, kann das Verschieben der Form in Microsoft Word auch den Anker der Form verschieben.

## Beispiele



Zeigt, wie man den Absatzanker einer Form sperrt oder entsperrt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

builder->Write(u"Our shape will have an anchor attached to this paragraph.");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 160);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

builder->Writeln(u"Hello again!");

// Setzen Sie die Eigenschaft "AnchorLocked" auf "true", um den Anker der Form zu verhindern
// vom Bewegen, wenn die Form in Microsoft Word verschoben wird.
// Setzen Sie die Eigenschaft "AnchorLocked" auf "false", um jede Bewegung der Form zu ermöglichen
// um auch seinen Anker zu einem anderen Absatz zu verschieben, dem die Form nahe kommt.
shape->set_AnchorLocked(anchorLocked);

// Wenn die Form kein sichtbares Ankersymbol links von ihr hat,
// müssen wir sichtbare Anker über "Optionen" -> "Anzeige" -> "Objektanker" aktivieren.
doc->Save(get_ArtifactsDir() + u"Shape.AnchorLocked.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
