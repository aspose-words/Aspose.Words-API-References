---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs class"
linktitle: "ImageFieldMergingArgs"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs class. Fornisce dati per l'evento ImageFieldMerging(). Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class


Fornisce dati per l'evento [ImageFieldMerging()](../ifieldmergingcallback/imagefieldmerging/). Per saperne di più, visita l'articolo della documentazione [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class ImageFieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Restituisce l'oggetto [Document](../fieldmergingargsbase/get_document/) per il quale viene eseguita l'unione di posta. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Ottiene il nome del campo di unione come specificato nel documento. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Ottiene l'oggetto che rappresenta il campo di unione corrente. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Ottiene il nome del campo di unione nella fonte dati. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Ottiene il valore del campo dalla fonte dati. |
| [get_Image](./get_image/)() const | Specifica l'immagine che il motore di stampa unione deve inserire nel documento. |
| [get_ImageFileName](./get_imagefilename/)() const | Imposta il nome file dell'immagine che il motore di stampa unione deve inserire nel documento. |
| [get_ImageHeight](./get_imageheight/)() const | Specifica l'altezza dell'immagine da inserire nel documento. |
| [get_ImageStream](./get_imagestream/)() const | Specifica lo stream da cui il motore di stampa unione deve leggere un'immagine. |
| [get_ImageWidth](./get_imagewidth/)() const | Specifica la larghezza dell'immagine da inserire nel documento. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Ottiene l'indice basato su zero del record che viene unito. |
| [get_Shape](./get_shape/)() const | Specifica la forma che il motore di stampa unione deve inserire nel documento. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Ottiene il nome della tabella dati per l'operazione di unione corrente o una stringa vuota se il nome non è disponibile. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Imposta il valore del campo dalla fonte dati. |
| [set_Image](./set_image/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Specifica l'immagine che il motore di stampa unione deve inserire nel documento. |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Imposta il nome file dell'immagine che il motore di stampa unione deve inserire nel documento. |
| [set_ImageHeight](./set_imageheight/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Impostatore per [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageHeight](./get_imageheight/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Specifica lo stream da cui il motore di stampa unione deve leggere un'immagine. |
| [set_ImageStream](./set_imagestream/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [set_ImageWidth](./set_imagewidth/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Impostatore per [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth](./get_imagewidth/). |
| [set_Shape](./set_shape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Impostatore per [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape](./get_shape/). |
| static [Type](./type/)() |  |
## Note


Questo evento si verifica durante la stampa unione quando viene incontrato un campo di stampa unione immagine nel documento. È possibile rispondere a questo evento restituendo un nome file, uno stream o un oggetto **Image** al motore di stampa unione affinché venga inserito nel documento.

Sono disponibili tre proprietà [ImageFileName](./get_imagefilename/), [ImageStream](./get_imagestream/) e [Image](./get_image/) per specificare da dove deve essere prelevata l'immagine. Impostare solo una di queste proprietà.

Per inserire un campo di stampa unione immagine in un documento di Word, selezionare il comando Inserisci/Campo, quindi scegliere UnisciCampo e digitare Image:MyFieldName.

## Vedi anche

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
