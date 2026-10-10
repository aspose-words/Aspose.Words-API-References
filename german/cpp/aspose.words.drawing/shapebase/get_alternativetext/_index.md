---
title: "Aspose::Words::Drawing::ShapeBase::get_AlternativeText Methode"
linktitle: "get_AlternativeText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_AlternativeText Methode. Definiert alternativen Text, der anstelle einer Grafik in C++ angezeigt wird."
type: docs
weight: 4000
url: /de/cpp/aspose.words.drawing/shapebase/get_alternativetext/
---
## ShapeBase::get_AlternativeText method


Definiert alternativen Text, der anstelle einer Grafik angezeigt wird.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_AlternativeText()
```

## Hinweise


Der Standardwert ist eine leere Zeichenfolge.

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
