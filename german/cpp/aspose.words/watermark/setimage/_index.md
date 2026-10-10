---
title: "Aspose::Words::Watermark::SetImage Methode"
linktitle: "SetImage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Watermark::SetImage Methode. Fügt ein Bildwasserzeichen in das Dokument in C++ ein."
type: docs
weight: 6000
url: /de/cpp/aspose.words/watermark/setimage/
---
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Fügt ein Bildwasserzeichen in das Dokument ein.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Bild | const System::SharedPtr\<System::Drawing::Image\>\& | Bild, das als Wasserzeichen angezeigt wird. |

## Beispiele



Zeigt, wie man ein Wasserzeichen aus einem Bild im lokalen Dateisystem erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ändern Sie das Aussehen des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt,
// und übergeben Sie es beim Erstellen eines Wasserzeichens aus einer Bilddatei.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Wir haben verschiedene Optionen, um ein Bild einzufügen.
// Verwenden Sie eine der folgenden Methoden, um ein Bildwasserzeichen hinzuzufügen.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Siehe auch

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Fügt ein Bildwasserzeichen in das Dokument ein.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Bild | const System::SharedPtr\<System::Drawing::Image\>\& | Bild, das als Wasserzeichen angezeigt wird. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

## Beispiele



Zeigt, wie man ein Wasserzeichen aus einem Bild im lokalen Dateisystem erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ändern Sie das Aussehen des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt,
// und übergeben Sie es beim Erstellen eines Wasserzeichens aus einer Bilddatei.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Wir haben verschiedene Optionen, um ein Bild einzufügen.
// Verwenden Sie eine der folgenden Methoden, um ein Bildwasserzeichen hinzuzufügen.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Siehe auch

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Fügt ein Bildwasserzeichen in das Dokument ein.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::IO::Stream> &imageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageStream | const System::SharedPtr\<System::IO::Stream\>\& | Der Stream, der die Bilddaten enthält, die als Wasserzeichen angezeigt werden. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

## Beispiele



Zeigt, wie man ein Wasserzeichen aus einem Bild-Stream erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ändern Sie das Aussehen des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt,
// und übergeben Sie es beim Erstellen eines Wasserzeichens aus einer Bilddatei.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);

{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open, System::IO::FileAccess::Read);
    doc->get_Watermark()->SetImage(imageStream, imageWatermarkOptions);
}

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermarkStream.docx");
```

## Siehe auch

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Fügt ein Bildwasserzeichen in das Dokument ein.

```cpp
void Aspose::Words::Watermark::SetImage(const System::String &imagePath, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imagePath | const System::String\& | Pfad zur Bilddatei, die als Wasserzeichen angezeigt wird. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Definiert zusätzliche Optionen für das Bildwasserzeichen. |

## Beispiele



Zeigt, wie man ein Wasserzeichen aus einem Bild im lokalen Dateisystem erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ändern Sie das Aussehen des Bildwasserzeichens mit einem ImageWatermarkOptions-Objekt,
// und übergeben Sie es beim Erstellen eines Wasserzeichens aus einer Bilddatei.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Wir haben verschiedene Optionen, um ein Bild einzufügen.
// Verwenden Sie eine der folgenden Methoden, um ein Bildwasserzeichen hinzuzufügen.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Siehe auch

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
