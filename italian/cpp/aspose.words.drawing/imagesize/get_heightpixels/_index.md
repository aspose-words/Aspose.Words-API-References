---
title: "Aspose::Words::Drawing::ImageSize::get_HeightPixels metodo"
linktitle: "get_HeightPixels"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ImageSize::get_HeightPixels metodo. Ottiene l'altezza dell'immagine in pixel in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.drawing/imagesize/get_heightpixels/
---
## ImageSize::get_HeightPixels method


Restituisce l'altezza dell'immagine in pixel.

```cpp
int32_t Aspose::Words::Drawing::ImageSize::get_HeightPixels() const
```


## Esempi



Mostra come leggere le proprietà di un'immagine in una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una forma nel documento che contiene un'immagine prelevata dal nostro file system locale.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Se la forma contiene un'immagine, la sua proprietà ImageData sarà valida,
// e conterrà un oggetto ImageSize.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

// L'oggetto ImageSize contiene informazioni di sola lettura sull'immagine all'interno della forma.
ASSERT_EQ(400, imageSize->get_HeightPixels());
ASSERT_EQ(400, imageSize->get_WidthPixels());

const double delta = 0.05;
ASSERT_NEAR(95.98, imageSize->get_HorizontalResolution(), delta);
ASSERT_NEAR(95.98, imageSize->get_VerticalResolution(), delta);

// Possiamo basare le dimensioni della forma sulla dimensione della sua immagine per evitare di allungare l'immagine.
shape->set_Width(imageSize->get_WidthPoints() * 2);
shape->set_Height(imageSize->get_HeightPoints() * 2);

doc->Save(get_ArtifactsDir() + u"Drawing.ImageSize.docx");
```

## Vedi anche

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
