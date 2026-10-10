---
title: "Metodo Aspose::Words::Drawing::Fill::SetImage"
linktitle: "SetImage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Fill::SetImage. Cambia il tipo di riempimento in immagine singola in C++."
type: docs
weight: 42000
url: /it/cpp/aspose.words.drawing/fill/setimage/
---
## Fill::SetImage(const System::ArrayPtr\<uint8_t\>\&) method


Cambia il tipo di riempimento in immagine singola.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::ArrayPtr<uint8_t> &imageBytes)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageBytes | const System::ArrayPtr\<uint8_t\>\& | L'array di byte dell'immagine. |

## Esempi



Mostra come impostare il tipo di riempimento della forma come immagine.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Esistono diversi modi per impostare l'immagine.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  Utilizzando un nome file locale del sistema:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  Carica un file in un array di byte:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  Da un flusso:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## Vedi anche

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::SetImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Cambia il tipo di riempimento in immagine singola.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Il flusso che contiene i byte dell'immagine. |

## Esempi



Mostra come impostare il tipo di riempimento della forma come immagine.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Esistono diversi modi per impostare l'immagine.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  Utilizzando un nome file locale del sistema:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  Carica un file in un array di byte:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  Da un flusso:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## Vedi anche

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::SetImage(const System::String\&) method


Cambia il tipo di riempimento in immagine singola.

```cpp
void Aspose::Words::Drawing::Fill::SetImage(const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Il percorso al file immagine. |

## Esempi



Mostra come impostare il tipo di riempimento della forma come immagine.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Esistono diversi modi per impostare l'immagine.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 1 -  Utilizzando un nome file locale del sistema:
shape->get_Fill()->SetImage(get_ImageDir() + u"Logo.jpg");
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.FileName.docx");

// 2 -  Carica un file in un array di byte:
shape->get_Fill()->SetImage(System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg"));
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.ByteArray.docx");

// 3 -  Da un flusso:
{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    shape->get_Fill()->SetImage(stream);
}
doc->Save(get_ArtifactsDir() + u"Shape.FillImage.Stream.docx");
```

## Vedi anche

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
