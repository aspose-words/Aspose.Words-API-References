---
title: "Aspose::Words::Drawing::ImageData::SetImage method"
linktitle: "SetImage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ImageData::SetImage method. Imposta l'immagine che la forma visualizza in C++."
type: docs
weight: 35000
url: /it/cpp/aspose.words.drawing/imagedata/setimage/
---
## ImageData::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Imposta l'immagine visualizzata dalla forma.

```cpp
void Aspose::Words::Drawing::ImageData::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | L'oggetto immagine. |

## Vedi anche

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## ImageData::SetImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Imposta l'immagine visualizzata dalla forma.

```cpp
void Aspose::Words::Drawing::ImageData::SetImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Lo stream che contiene l'immagine. |

## Vedi anche

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## ImageData::SetImage(const System::String\&) method


Imposta l'immagine visualizzata dalla forma.

```cpp
void Aspose::Words::Drawing::ImageData::SetImage(const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Il file immagine. Può essere un nome file o un URL. |

## Esempi



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

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## ImageData::SetImage(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::ImageData::SetImage(std::basic_istream<CharType, Traits> &stream)
```

## Vedi anche

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
