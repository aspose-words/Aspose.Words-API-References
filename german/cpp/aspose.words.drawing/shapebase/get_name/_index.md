---
title: "Aspose::Words::Drawing::ShapeBase::get_Name method"
linktitle: "get_Name"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_Name-Methode. Ruft den optionalen Formnamen in C++ ab oder legt ihn fest."
type: docs
weight: 40000
url: /de/cpp/aspose.words.drawing/shapebase/get_name/
---
## ShapeBase::get_Name method


Liest oder legt den optionalen Namen der Form fest.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Name()
```

## Hinweise


Standard ist ein leerer String.

Darf nicht **null** sein, kann aber eine leere Zeichenkette sein.

## Beispiele



Zeigt, wie man den Alternativtext einer Form verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 150, 150);
shape->set_Name(u"MyCube");

shape->set_AlternativeText(u"Alt text for MyCube.");

// Wir können den Alternativtext einer Form über einen Rechtsklick und anschließend über "Format AutoShape" -> "Alt Text" aufrufen.
doc->Save(get_ArtifactsDir() + u"Shape.AltText.docx");

// Speichern Sie das Dokument als HTML und löschen Sie anschließend das verknüpfte Bild, das zu unserer Form gehört.
// Der Browser, der unser HTML liest, zeigt den Alt‑Text anstelle des fehlenden Bildes an.
doc->Save(get_ArtifactsDir() + u"Shape.AltText.html");
System::IO::File::Delete(get_ArtifactsDir() + u"Shape.AltText.001.png");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
