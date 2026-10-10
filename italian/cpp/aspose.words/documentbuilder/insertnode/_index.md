---
title: "Metodo Aspose::Words::DocumentBuilder::InsertNode"
linktitle: "InsertNode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::InsertNode. Inserisce un nodo prima del cursore in C++."
type: docs
weight: 40000
url: /it/cpp/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder::InsertNode method


Inserisce un nodo prima del cursore.

```cpp
void Aspose::Words::DocumentBuilder::InsertNode(const System::SharedPtr<Aspose::Words::Node> &node)
```


## Esempi



Mostra come inserire un'immagine collegata in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFileName = get_ImageDir() + u"Windows MetaFile.wmf";

// Di seguito sono riportati due modi per applicare un'immagine a una forma in modo che possa visualizzarla.
// 1 -  Imposta la forma per contenere l'immagine.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx");

// Ogni immagine che memorizziamo nella forma aumenterà le dimensioni del nostro documento.
ASSERT_TRUE(70000 < System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 -  Imposta la forma per collegarsi a un file immagine nel file system locale.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx");

// Collegare le immagini farà risparmiare spazio e produrrà un documento più piccolo.
// Tuttavia, il documento può visualizzare correttamente l'immagine solo finché
// il file immagine è presente nella posizione a cui punta la proprietà \"SourceFullName\" della forma.
ASSERT_TRUE(10000 > System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## Vedi anche

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
