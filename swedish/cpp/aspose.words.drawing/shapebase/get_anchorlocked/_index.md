---
title: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked‑metod"
linktitle: "get_AnchorLocked"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_AnchorLocked‑metod. Anger om formens ankare är låst i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.drawing/shapebase/get_anchorlocked/
---
## ShapeBase::get_AnchorLocked method


Anger om formens ankare är låst.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AnchorLocked()
```

## Anmärkningar


Standardvärdet är **false**.

Har endast effekt för former på toppnivå.

Denna egenskap påverkar beteendet för formens ankare i Microsoft Word. När ankaret inte är låst kan flyttning av formen i Microsoft Word också flytta formens ankare.

## Exempel



Visar hur man låser eller låser upp en forms paragrafankare.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

builder->Write(u"Our shape will have an anchor attached to this paragraph.");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 160);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

builder->Writeln(u"Hello again!");

// Ställ in egenskapen "AnchorLocked" till "true" för att förhindra formens ankare
// från att flyttas när formen flyttas i Microsoft Word.
// Ställ in egenskapen "AnchorLocked" till "false" för att tillåta alla rörelser av formen
// för att även flytta dess ankare till vilket annat stycke som helst som formen hamnar nära.
shape->set_AnchorLocked(anchorLocked);

// Om formen inte har en synlig ankarsymbol till vänster,
// behöver vi aktivera synliga ankare via "Options" -> "Display" -> "Object Anchors".
doc->Save(get_ArtifactsDir() + u"Shape.AnchorLocked.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
