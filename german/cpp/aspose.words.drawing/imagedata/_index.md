---
title: "Aspose::Words::Drawing::ImageData class"
linktitle: "ImageData"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ImageData class. Definiert ein Bild für eine shape. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing/imagedata/
---
## ImageData class


Definiert ein Bild für eine Form. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/).

```cpp
class ImageData : public Aspose::Words::IBorderAttrSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [FitImageToShape](./fitimagetoshape/)() | Passt die Bilddaten an den [Shape](../shape/)-Rahmen an, sodass das Seitenverhältnis der Bilddaten dem Seitenverhältnis des [Shape](../shape/)-Rahmens entspricht. |
| [get_BiLevel](./get_bilevel/)() | Bestimmt, ob ein Bild in Schwarz‑Weiß angezeigt wird. |
| [get_Borders](./get_borders/)() | Ruft die Sammlung der Bildränder ab. Ränder wirken nur bei Inline‑Bildern. |
| [get_Brightness](./get_brightness/)() | Liest oder legt die Helligkeit des Bildes fest. Der Wert dieser Eigenschaft muss eine Zahl zwischen 0,0 (dunkelste) und 1,0 (hellste) sein. |
| [get_ChromaKey](./get_chromakey/)() | Definiert den Farbwert des Bildes, der als transparent behandelt wird. |
| [get_Contrast](./get_contrast/)() | Liest oder legt den Kontrast des angegebenen Bildes fest. Der Wert dieser Eigenschaft muss eine Zahl zwischen 0,0 (geringster Kontrast) und 1,0 (höchster Kontrast) sein. |
| [get_CropBottom](./get_cropbottom/)() | Definiert den Anteil des Bildausschnitts, der von der Unterseite entfernt wird. |
| [get_CropLeft](./get_cropleft/)() | Definiert den Anteil des Bildausschnitts, der von der linken Seite entfernt wird. |
| [get_CropRight](./get_cropright/)() | Definiert den Anteil des Bildausschnitts, der von der rechten Seite entfernt wird. |
| [get_CropTop](./get_croptop/)() | Definiert den Anteil des Bildausschnitts, der von der Oberseite entfernt wird. |
| [get_GrayScale](./get_grayscale/)() | Bestimmt, ob ein Bild im Graustufenmodus angezeigt wird. |
| [get_HasImage](./get_hasimage/)() | Gibt **true** zurück, wenn die shape Bildbytes enthält oder ein Bild verlinkt. |
| [get_ImageBytes](./get_imagebytes/)() | Liest oder legt die Rohbytes des in der shape gespeicherten Bildes fest. |
| [get_ImageSize](./get_imagesize/)() | Ruft die Informationen zur Bildgröße und Auflösung ab. |
| [get_ImageType](./get_imagetype/)() | Ermittelt den Typ des Bildes. |
| [get_IsLink](./get_islink/)() | Gibt **true** zurück, wenn das Bild mit der Form verknüpft ist (wenn [SourceFullName](./get_sourcefullname/) angegeben ist). |
| [get_IsLinkOnly](./get_islinkonly/)() | Gibt **true** zurück, wenn das Bild verknüpft und nicht im Dokument gespeichert ist. |
| [get_SourceFullName](./get_sourcefullname/)() | Liest oder legt den Pfad und Namen der Quelldatei für das verknüpfte Bild fest. |
| [get_Title](./get_title/)() | Definiert den Titel eines Bildes. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Speichert das Bild in den angegebenen Stream. |
| [Save](./save/)(const System::String\&) | Speichert das Bild in einer Datei. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_BiLevel](./set_bilevel/)(bool) | Setter für [Aspose::Words::Drawing::ImageData::get_BiLevel](./get_bilevel/). |
| [set_Brightness](./set_brightness/)(double) | Setter für [Aspose::Words::Drawing::ImageData::get_Brightness](./get_brightness/). |
| [set_ChromaKey](./set_chromakey/)(System::Drawing::Color) | Setter für [Aspose::Words::Drawing::ImageData::get_ChromaKey](./get_chromakey/). |
| [set_Contrast](./set_contrast/)(double) | Setter für [Aspose::Words::Drawing::ImageData::get_Contrast](./get_contrast/). |
| [set_CropBottom](./set_cropbottom/)(double) | Setter für [Aspose::Words::Drawing::ImageData::get_CropBottom](./get_cropbottom/). |
| [set_CropLeft](./set_cropleft/)(double) | Setter für [Aspose::Words::Drawing::ImageData::get_CropLeft](./get_cropleft/). |
| [set_CropRight](./set_cropright/)(double) | Setter für [Aspose::Words::Drawing::ImageData::get_CropRight](./get_cropright/). |
| [set_CropTop](./set_croptop/)(double) | Setter für [Aspose::Words::Drawing::ImageData::get_CropTop](./get_croptop/). |
| [set_GrayScale](./set_grayscale/)(bool) | Setter für [Aspose::Words::Drawing::ImageData::get_GrayScale](./get_grayscale/). |
| [set_ImageBytes](./set_imagebytes/)(const System::ArrayPtr\<uint8_t\>\&) | Setter für [Aspose::Words::Drawing::ImageData::get_ImageBytes](./get_imagebytes/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ImageData::get_SourceFullName](./get_sourcefullname/). |
| [set_Title](./set_title/)(const System::String\&) | Setter für [Aspose::Words::Drawing::ImageData::get_Title](./get_title/). |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Legt das Bild fest, das die Form anzeigt. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Legt das Bild fest, das die Form anzeigt. |
| [SetImage](./setimage/)(const System::String\&) | Legt das Bild fest, das die Form anzeigt. |
| [SetImage](./setimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [ToByteArray](./tobytearray/)() | Gibt Bildbytes für jedes Bild zurück, unabhängig davon, ob das Bild gespeichert oder verknüpft ist. |
| [ToImage](./toimage/)() | Liest das in der Form gespeicherte Bild als **Image**-Objekt. |
| [ToStream](./tostream/)() | Erstellt und gibt einen Stream zurück, der die Bildbytes enthält. |
| static [Type](./type/)() |  |
## Hinweise


Verwenden Sie die Eigenschaft [ImageData](../shape/get_imagedata/), um auf das Bild in einer Form zuzugreifen und es zu ändern. Sie erstellen keine Instanzen der Klasse [ImageData](./) direkt.

Ein Bild kann in einer Form gespeichert, mit einer externen Datei verknüpft oder beides sein (verknüpft und im Dokument gespeichert).

Unabhängig davon, ob das Bild innerhalb der Form gespeichert oder verknüpft ist, können Sie jederzeit auf das eigentliche Bild zugreifen, indem Sie die Methoden [ToByteArray](./tobytearray/), [ToStream](./tostream/), [ToImage](./toimage/) oder [Save()](../) verwenden. Wenn das Bild innerhalb der Form gespeichert ist, können Sie es auch direkt über die Eigenschaft [ImageBytes](./get_imagebytes/) abrufen.

Um ein Bild in einer Form zu speichern, verwenden Sie die Methode [SetImage()](../). Um ein Bild mit einer Form zu verknüpfen, setzen Sie die Eigenschaft [SourceFullName](./get_sourcefullname/).

## Beispiele



Zeigt, wie Bilder aus einem Dokument extrahiert und als einzelne Dateien im lokalen Dateisystem gespeichert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Holen Sie die Sammlung von Formen aus dem Dokument,
// und speichern Sie die Bilddaten jeder Form, die ein Bild enthält, als Datei im lokalen Dateisystem.
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
        // Die Bilddaten von Formen können Bilder in vielen möglichen Bildformaten enthalten.
        // Wir können für jedes Bild automatisch eine Dateierweiterung basierend auf seinem Format bestimmen.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
