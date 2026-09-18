---
title: "Aspose::Words::Drawing::Fill::SetImage-Methode"
linktitle: "SetImage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Fill::SetImage-Methode. Ändert den Fülltyp zu einem einzelnen Bild in C++."
type: docs
weight: 42000
url: /de/cpp/aspose.words.drawing/fill/setimage/
---
## Fill::SetImage(const System::ArrayPtr\<uint8_t\>\&) method


Ändert den Fülltyp zu einem einzelnen Bild.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | Das Bild‑Byte‑Array. |

## Beispiele



Zeigt, wie man den Fülltyp einer Form als Bild festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Es gibt mehrere Möglichkeiten, ein Bild festzulegen.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  Verwendung eines lokalen Systemdateinamens:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  Laden einer Datei in ein Byte‑Array:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  Aus einem Stream:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## Siehe auch

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::SetImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Ändert den Fülltyp zu einem einzelnen Bild.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Der Stream, der die Bild‑Bytes enthält. |

## Beispiele



Zeigt, wie man den Fülltyp einer Form als Bild festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Es gibt mehrere Möglichkeiten, ein Bild festzulegen.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  Verwendung eines lokalen Systemdateinamens:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  Laden einer Datei in ein Byte‑Array:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  Aus einem Stream:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## Siehe auch

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::SetImage(const System::String\&) method


Ändert den Fülltyp zu einem einzelnen Bild.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::String &fileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Der Pfad zur Bilddatei. |

## Beispiele



Zeigt, wie man den Fülltyp einer Form als Bild festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Es gibt mehrere Möglichkeiten, ein Bild festzulegen.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  Verwendung eines lokalen Systemdateinamens:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  Laden einer Datei in ein Byte‑Array:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  Aus einem Stream:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## Siehe auch

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
