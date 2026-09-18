---
title: "Aspose::Words::DocumentBuilder::InsertNode-Methode"
linktitle: "InsertNode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertNode-Methode. Fügt einen Knoten vor dem Cursor in C++ ein."
type: docs
weight: 40000
url: /de/cpp/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder::InsertNode method


Fügt einen Knoten vor dem Cursor ein.

```cpp
void Aspose::Words::DocumentBuilder::InsertNode(const System::SharedPtr<Aspose::Words::Node> &node)
```


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

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
