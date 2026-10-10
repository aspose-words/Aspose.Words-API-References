---
title: "Aspose::Words::Saving::ImageSaveOptions::get_Scale-Methode"
linktitle: "get_Scale"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSaveOptions::get_Scale-Methode. Gibt den Zoomfaktor für die erzeugten Bilder zurück oder legt ihn fest in C++."
type: docs
weight: 14000
url: /de/cpp/aspose.words.saving/imagesaveoptions/get_scale/
---
## ImageSaveOptions::get_Scale method


Liest oder setzt den Zoom‑Faktor für die erzeugten Bilder.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_Scale() const
```


## Beispiele



Zeigt, wie das Bild bearbeitet werden kann, während Aspose.Words ein Dokument konvertiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Wenn wir das Dokument als Bild speichern, können wir ein SaveOptions‑Objekt übergeben, um
// das Bild zu bearbeiten, während der Speichervorgang es rendert.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Wir können diese Eigenschaften anpassen, um die Helligkeit und den Kontrast des Bildes zu ändern.
// Beide liegen auf einer Skala von 0‑1 und haben standardmäßig 0,5.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Wir können die horizontale und vertikale Auflösung mit diesen Eigenschaften anpassen.
// Dies wirkt sich auf die Abmessungen des Bildes aus.
// Der Standardwert für diese Eigenschaften ist 96,0 bei einer Auflösung von 96 dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Wir können das Bild mit dieser Eigenschaft skalieren. Der Standardwert ist 1,0 für eine Skalierung von 100 %.
// Wir können diese Eigenschaft verwenden, um Änderungen der Bildabmessungen, die durch eine Auflösungsänderung entstehen würden, zu neutralisieren.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```


Zeigt, wie man ein Office‑[Math](../../../aspose.words.math/)-Objekt in eine Bilddatei im lokalen Dateisystem rendert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Erstellen Sie ein "ImageSaveOptions"-Objekt, um es an die "Save"-Methode des Knoten-Renderers zu übergeben, um zu ändern
// wie es den OfficeMath-Knoten in ein Bild rendert.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Setzen Sie die Eigenschaft "Scale" auf 5, um das Objekt fünfmal so groß wie die Originalgröße zu rendern.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Siehe auch

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
