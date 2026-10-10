---
title: "Aspose::Words::Drawing::ImageData::get_SourceFullName Methode"
linktitle: "get_SourceFullName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ImageData::get_SourceFullName Methode. Ruft den Pfad und Namen der Quelldatei für das verknüpfte Bild in C++ ab oder legt ihn fest."
type: docs
weight: 18000
url: /de/cpp/aspose.words.drawing/imagedata/get_sourcefullname/
---
## ImageData::get_SourceFullName method


Liest oder legt den Pfad und Namen der Quelldatei für das verknüpfte Bild fest.

```cpp
System::String Aspose::Words::Drawing::ImageData::get_SourceFullName()
```

## Hinweise


Der Standardwert ist eine leere Zeichenfolge.

Wenn [SourceFullName](./) kein leerer String ist, ist das Bild verknüpft.

## Beispiele



Zeigt, wie ein verknüpftes Bild in ein Dokument eingefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFileName = get_ImageDir() + u"Windows MetaFile.wmf";

// Im Folgenden werden zwei Methoden gezeigt, ein Bild einer Form zuzuweisen, damit sie es anzeigen kann.
// 1 –  Setzen Sie die Form so, dass sie das Bild enthält.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx");

// Jedes Bild, das wir in einer Form speichern, vergrößert die Größe unseres Dokuments.
ASSERT_TRUE(70000 < System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 –  Setzen Sie die Form so, dass sie zu einer Bilddatei im lokalen Dateisystem verlinkt.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx");

// Das Verknüpfen von Bildern spart Speicherplatz und führt zu einem kleineren Dokument.
// Allerdings kann das Dokument das Bild nur korrekt anzeigen, solange
// die Bilddatei am Ort vorhanden ist, auf den die Eigenschaft "SourceFullName" der Form verweist.
ASSERT_TRUE(10000 > System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## Siehe auch

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
