---
title: "Aspose::Words::Drawing::ImageSize::get_WidthPixels metodo"
linktitle: "get_WidthPixels"
second_title: "Riferimento API Aspose.Words per C++"
description: "metodo Aspose::Words::Drawing::ImageSize::get_WidthPixels. Ottiene la larghezza dell'immagine in pixel in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.drawing/imagesize/get_widthpixels/
---
## ImageSize::get_WidthPixels method


Restituisce la larghezza dell'immagine in pixel.

```cpp
int32_t Aspose::Words::Drawing::ImageSize::get_WidthPixels() const
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
