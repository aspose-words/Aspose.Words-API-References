---
title: "Aspose::Words::Drawing::ImageData::get_Contrast-Methode"
linktitle: "get_Contrast"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ImageData::get_Contrast-Methode. Ruft den Kontrast des angegebenen Bildes ab oder legt ihn fest. Der Wert dieser Eigenschaft muss eine Zahl zwischen 0,0 (geringster Kontrast) und 1,0 (höchster Kontrast) in C++ sein."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing/imagedata/get_contrast/
---
## ImageData::get_Contrast method


Liest oder legt den Kontrast des angegebenen Bildes fest. Der Wert dieser Eigenschaft muss eine Zahl zwischen 0,0 (geringster Kontrast) und 1,0 (höchster Kontrast) sein.

```cpp
double Aspose::Words::Drawing::ImageData::get_Contrast()
```

## Hinweise


Der Standardwert ist 0,5.

## Beispiele



Zeigt, wie man die Bilddaten einer Form bearbeitet.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");
auto sourceShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

auto dstDoc = System::MakeObject<Aspose::Words::Document>();

// Importieren Sie eine Form aus dem Quelldokument und fügen Sie sie dem ersten Absatz hinzu.
auto importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

// Die importierte Form enthält ein Bild. Wir können über das ImageData-Objekt auf die Bildeigenschaften und Rohdaten zugreifen.
System::SharedPtr<Aspose::Words::Drawing::ImageData> imageData = importedShape->get_ImageData();
imageData->set_Title(u"Imported Image");

ASSERT_TRUE(imageData->get_HasImage());

// Wenn ein Bild keine Ränder hat, definiert sein ImageData-Objekt die Randfarbe als leer.
ASSERT_EQ(4, imageData->get_Borders()->get_Count());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, imageData->get_Borders()->idx_get(0)->get_Color());

// Dieses Bild verlinkt nicht zu einer anderen Form oder Bilddatei im lokalen Dateisystem.
ASSERT_FALSE(imageData->get_IsLink());
ASSERT_FALSE(imageData->get_IsLinkOnly());

// Die Eigenschaften "Brightness" und "Contrast" definieren die Bildhelligkeit und den Kontrast.
// auf einer Skala von 0 bis 1, wobei der Standardwert bei 0,5 liegt.
imageData->set_Brightness(0.8);
imageData->set_Contrast(1.0);

// Die obigen Helligkeits- und Kontrastwerte haben ein Bild mit viel Weiß erzeugt.
// Wir können mit der ChromaKey-Eigenschaft eine Farbe auswählen, die durch Transparenz ersetzt werden soll, zum Beispiel Weiß.
imageData->set_ChromaKey(System::Drawing::Color::get_White());

// Importieren Sie die Quellform erneut und setzen Sie das Bild auf monochrom.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_GrayScale(true);

// Importieren Sie die Quellform erneut, um ein drittes Bild zu erstellen, und setzen Sie es auf BiLevel.
// BiLevel setzt jedes Pixel entweder auf Schwarz oder Weiß, je nachdem, welche Farbe dem Originalfarbwert näher liegt.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_BiLevel(true);

// Das Zuschneiden wird auf einer Skala von 0 bis 1 bestimmt. Einen Rand um 0,3 zuschneiden
// schneidet 30 % des Bildes an der beschnittenen Seite ab.
importedShape->get_ImageData()->set_CropBottom(0.3);
importedShape->get_ImageData()->set_CropLeft(0.3);
importedShape->get_ImageData()->set_CropTop(0.3);
importedShape->get_ImageData()->set_CropRight(0.3);

dstDoc->Save(get_ArtifactsDir() + u"Drawing.ImageData.docx");
```

## Siehe auch

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
