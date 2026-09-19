---
title: "Aspose::Words::Drawing::ImageData class"
linktitle: "ImageData"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ImageData class. Definisce un'immagine per una forma. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.drawing/imagedata/
---
## ImageData class


Definisce un'immagine per una forma. Per saperne di più, visita l'articolo di documentazione [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/).

```cpp
class ImageData : public Aspose::Words::IBorderAttrSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [FitImageToShape](./fitimagetoshape/)() | Adatta i dati dell'immagine al riquadro [Shape](../shape/) in modo che il rapporto d'aspetto dei dati dell'immagine corrisponda al rapporto d'aspetto del riquadro [Shape](../shape/). |
| [get_BiLevel](./get_bilevel/)() | Determina se un'immagine verrà visualizzata in bianco e nero. |
| [get_Borders](./get_borders/)() | Ottiene la raccolta dei bordi dell'immagine. I bordi hanno effetto solo per le immagini in linea. |
| [get_Brightness](./get_brightness/)() | Ottiene o imposta la luminosità dell'immagine. Il valore di questa proprietà deve essere un numero compreso tra 0.0 (più scuro) e 1.0 (più luminoso). |
| [get_ChromaKey](./get_chromakey/)() | Definisce il valore di colore dell'immagine che sarà trattato come trasparente. |
| [get_Contrast](./get_contrast/)() | Ottiene o imposta il contrasto per l'immagine specificata. Il valore di questa proprietà deve essere un numero compreso tra 0.0 (meno contrasto) e 1.0 (massimo contrasto). |
| [get_CropBottom](./get_cropbottom/)() | Definisce la frazione di rimozione dell'immagine dal lato inferiore. |
| [get_CropLeft](./get_cropleft/)() | Definisce la frazione di rimozione dell'immagine dal lato sinistro. |
| [get_CropRight](./get_cropright/)() | Definisce la frazione di rimozione dell'immagine dal lato destro. |
| [get_CropTop](./get_croptop/)() | Definisce la frazione di rimozione dell'immagine dal lato superiore. |
| [get_GrayScale](./get_grayscale/)() | Determina se un'immagine verrà visualizzata in modalità scala di grigi. |
| [get_HasImage](./get_hasimage/)() | Restituisce **true** se la forma contiene byte dell'immagine o collega un'immagine. |
| [get_ImageBytes](./get_imagebytes/)() | Ottiene o imposta i byte grezzi dell'immagine memorizzata nella forma. |
| [get_ImageSize](./get_imagesize/)() | Ottiene le informazioni sulla dimensione e sulla risoluzione dell'immagine. |
| [get_ImageType](./get_imagetype/)() | Ottiene il tipo dell'immagine. |
| [get_IsLink](./get_islink/)() | Restituisce **true** se l'immagine è collegata alla forma (quando è specificato [SourceFullName](./get_sourcefullname/)). |
| [get_IsLinkOnly](./get_islinkonly/)() | Restituisce **true** se l'immagine è collegata e non è memorizzata nel documento. |
| [get_SourceFullName](./get_sourcefullname/)() | Ottiene o imposta il percorso e il nome del file sorgente per l'immagine collegata. |
| [get_Title](./get_title/)() | Definisce il titolo di un'immagine. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Salva l'immagine nello stream specificato. |
| [Save](./save/)(const System::String\&) | Salva l'immagine in un file. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_BiLevel](./set_bilevel/)(bool) | Setter per [Aspose::Words::Drawing::ImageData::get_BiLevel](./get_bilevel/). |
| [set_Brightness](./set_brightness/)(double) | Setter per [Aspose::Words::Drawing::ImageData::get_Brightness](./get_brightness/). |
| [set_ChromaKey](./set_chromakey/)(System::Drawing::Color) | Setter per [Aspose::Words::Drawing::ImageData::get_ChromaKey](./get_chromakey/). |
| [set_Contrast](./set_contrast/)(double) | Setter per [Aspose::Words::Drawing::ImageData::get_Contrast](./get_contrast/). |
| [set_CropBottom](./set_cropbottom/)(double) | Setter per [Aspose::Words::Drawing::ImageData::get_CropBottom](./get_cropbottom/). |
| [set_CropLeft](./set_cropleft/)(double) | Setter per [Aspose::Words::Drawing::ImageData::get_CropLeft](./get_cropleft/). |
| [set_CropRight](./set_cropright/)(double) | Setter per [Aspose::Words::Drawing::ImageData::get_CropRight](./get_cropright/). |
| [set_CropTop](./set_croptop/)(double) | Setter per [Aspose::Words::Drawing::ImageData::get_CropTop](./get_croptop/). |
| [set_GrayScale](./set_grayscale/)(bool) | Setter per [Aspose::Words::Drawing::ImageData::get_GrayScale](./get_grayscale/). |
| [set_ImageBytes](./set_imagebytes/)(const System::ArrayPtr\<uint8_t\>\&) | Setter per [Aspose::Words::Drawing::ImageData::get_ImageBytes](./get_imagebytes/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Setter per [Aspose::Words::Drawing::ImageData::get_SourceFullName](./get_sourcefullname/). |
| [set_Title](./set_title/)(const System::String\&) | Setter per [Aspose::Words::Drawing::ImageData::get_Title](./get_title/). |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Imposta l'immagine visualizzata dalla forma. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Imposta l'immagine visualizzata dalla forma. |
| [SetImage](./setimage/)(const System::String\&) | Imposta l'immagine visualizzata dalla forma. |
| [SetImage](./setimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [ToByteArray](./tobytearray/)() | Restituisce i byte dell'immagine per qualsiasi immagine, indipendentemente dal fatto che l'immagine sia memorizzata o collegata. |
| [ToImage](./toimage/)() | Ottiene l'immagine memorizzata nella forma come oggetto **Image**. |
| [ToStream](./tostream/)() | Crea e restituisce uno stream che contiene i byte dell'immagine. |
| static [Type](./type/)() |  |
## Note


Utilizza la proprietà [ImageData](../shape/get_imagedata/) per accedere e modificare l'immagine all'interno di una forma. Non crei istanze della classe [ImageData](./) direttamente.

Un'immagine può essere memorizzata all'interno di una forma, collegata a un file esterno o entrambe le opzioni (collegata e memorizzata nel documento).

Indipendentemente dal fatto che l'immagine sia memorizzata all'interno della forma o collegata, puoi sempre accedere all'immagine reale utilizzando i metodi [ToByteArray](./tobytearray/), [ToStream](./tostream/), [ToImage](./toimage/) o [Save()](../). Se l'immagine è memorizzata all'interno della forma, puoi anche accedervi direttamente tramite la proprietà [ImageBytes](./get_imagebytes/).

Per memorizzare un'immagine all'interno di una forma utilizza il metodo [SetImage()](../). Per collegare un'immagine a una forma, imposta la proprietà [SourceFullName](./get_sourcefullname/).

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
