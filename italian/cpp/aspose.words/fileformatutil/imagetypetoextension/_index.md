---
title: "Aspose::Words::FileFormatUtil::ImageTypeToExtension method"
linktitle: "ImageTypeToExtension"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::FileFormatUtil::ImageTypeToExtension method. Converte un valore enumerato di tipo immagine Aspose.Words in un'estensione di file. L'estensione restituita è una stringa in minuscolo con un punto iniziale in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil::ImageTypeToExtension method


Converte un valore enumerato di tipo immagine Aspose.Words in un'estensione di file. L'estensione restituita è una stringa in minuscolo con un punto iniziale.

```cpp
static System::String Aspose::Words::FileFormatUtil::ImageTypeToExtension(Aspose::Words::Drawing::ImageType imageType)
```


## Esempi



Mostra come estrarre le immagini da un documento e salvarle nel file system locale come file individuali.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Ottieni la raccolta di forme dal documento,
// e salva i dati dell'immagine di ogni forma contenente un'immagine come file nel file system locale.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // I dati dell'immagine delle forme possono contenere immagini in molti formati possibili.
        // Possiamo determinare automaticamente un'estensione file per ogni immagine, in base al suo formato.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```

## Vedi anche

* Enum [ImageType](../../../aspose.words.drawing/imagetype/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
