---
title: "Aspose::Words::Drawing::ImageData::get_SourceFullName metodo"
linktitle: "get_SourceFullName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ImageData::get_SourceFullName metodo. Ottiene o imposta il percorso e il nome del file sorgente per l'immagine collegata in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words.drawing/imagedata/get_sourcefullname/
---
## ImageData::get_SourceFullName method


Ottiene o imposta il percorso e il nome del file sorgente per l'immagine collegata.

```cpp
System::String Aspose::Words::Drawing::ImageData::get_SourceFullName()
```

## Note


Il valore predefinito è una stringa vuota.

Se [SourceFullName](./) non è una stringa vuota, l'immagine è collegata.

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

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
