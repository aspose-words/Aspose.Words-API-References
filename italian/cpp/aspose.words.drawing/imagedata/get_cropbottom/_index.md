---
title: "Aspose::Words::Drawing::ImageData::get_CropBottom method"
linktitle: "get_CropBottom"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ImageData::get_CropBottom method. Definisce la frazione di rimozione dell'immagine dal lato inferiore in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.drawing/imagedata/get_cropbottom/
---
## ImageData::get_CropBottom method


Definisce la frazione di rimozione dell'immagine dal lato inferiore.

```cpp
double Aspose::Words::Drawing::ImageData::get_CropBottom()
```

## Note


La quantità di ritaglio può variare da -1.0 a 1.0. Il valore predefinito è 0. Nota che un valore di 1 non mostrerà alcuna immagine. I valori negativi faranno sì che l'immagine venga compressa verso l'interno dal bordo ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato sarà riempito dal colore di riempimento della forma). I valori positivi inferiori a 1 faranno sì che l'immagine rimanente venga allungata per adattarsi alla forma.

Il valore predefinito è 0.

## Esempi



Mostra come modificare i dati immagine di una forma.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");
auto sourceShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

auto dstDoc = System::MakeObject<Aspose::Words::Document>();

// Importa una forma dal documento sorgente e aggiungila al primo paragrafo.
auto importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

// La forma importata contiene un'immagine. Possiamo accedere alle proprietà dell'immagine e ai dati grezzi tramite l'oggetto ImageData.
System::SharedPtr<Aspose::Words::Drawing::ImageData> imageData = importedShape->get_ImageData();
imageData->set_Title(u"Imported Image");

ASSERT_TRUE(imageData->get_HasImage());

// Se un'immagine non ha bordi, il suo oggetto ImageData definirà il colore del bordo come vuoto.
ASSERT_EQ(4, imageData->get_Borders()->get_Count());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, imageData->get_Borders()->idx_get(0)->get_Color());

// Questa immagine non è collegata a un'altra forma o a un file immagine nel file system locale.
ASSERT_FALSE(imageData->get_IsLink());
ASSERT_FALSE(imageData->get_IsLinkOnly());

// Le proprietà "Brightness" e "Contrast" definiscono la luminosità e il contrasto dell'immagine
// su una scala da 0 a 1, con valore predefinito a 0,5.
imageData->set_Brightness(0.8);
imageData->set_Contrast(1.0);

// I valori di luminosità e contrasto sopra indicati hanno creato un'immagine con molto bianco.
// Possiamo selezionare un colore con la proprietà ChromaKey da sostituire con trasparenza, ad esempio il bianco.
imageData->set_ChromaKey(System::Drawing::Color::get_White());

// Importa nuovamente la forma sorgente e imposta l'immagine in monocromo.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_GrayScale(true);

// Importa nuovamente la forma sorgente per creare una terza immagine e impostala su BiLevel.
// BiLevel imposta ogni pixel su nero o bianco, a seconda di quale sia più vicino al colore originale.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_BiLevel(true);

// Il ritaglio è determinato su una scala da 0-1. Ritagliare un lato di 0.3
// ritaglierà il 30% dell'immagine sul lato ritagliato.
importedShape->get_ImageData()->set_CropBottom(0.3);
importedShape->get_ImageData()->set_CropLeft(0.3);
importedShape->get_ImageData()->set_CropTop(0.3);
importedShape->get_ImageData()->set_CropRight(0.3);

dstDoc->Save(get_ArtifactsDir() + u"Drawing.ImageData.docx");
```

## Vedi anche

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
