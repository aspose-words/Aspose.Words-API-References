---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs class"
linktitle: "ImageFieldMergingArgs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs class. Tillhandahåller data för ImageFieldMerging()-händelsen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class


Tillhandahåller data för [ImageFieldMerging()](../ifieldmergingcallback/imagefieldmerging/)‑händelsen. För att lära dig mer, besök [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/)‑dokumentationsartikeln.

```cpp
class ImageFieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Returnerar [Document](../fieldmergingargsbase/get_document/)‑objektet för vilket kopplad sammanslagning utförs. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Hämtar namnet på sammanslagningsfältet enligt vad som anges i dokumentet. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Hämtar objektet som representerar det aktuella sammanslagningsfältet. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Hämtar namnet på sammanslagningsfältet i datakällan. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Hämtar värdet på fältet från datakällan. |
| [get_Image](./get_image/)() const | Anger bilden som kopplad sammanslagningsmotor måste infoga i dokumentet. |
| [get_ImageFileName](./get_imagefilename/)() const | Ställer in filnamnet på bilden som kopplad sammanslagningsmotor måste infoga i dokumentet. |
| [get_ImageHeight](./get_imageheight/)() const | Anger bildens höjd för bilden som ska infogas i dokumentet. |
| [get_ImageStream](./get_imagestream/)() const | Anger strömmen som mail merge‑motorn ska läsa en bild från. |
| [get_ImageWidth](./get_imagewidth/)() const | Anger bildens bredd för bilden som ska infogas i dokumentet. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Hämtar det nollbaserade indexet för posten som slås samman. |
| [get_Shape](./get_shape/)() const | Anger formen som mail merge‑motorn måste infoga i dokumentet. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Hämtar namnet på datatabellen för den aktuella sammanslagningsoperationen eller en tom sträng om namnet inte är tillgängligt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Ställer in värdet för fältet från datakällan. |
| [set_Image](./set_image/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Anger bilden som kopplad sammanslagningsmotor måste infoga i dokumentet. |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Ställer in filnamnet på bilden som kopplad sammanslagningsmotor måste infoga i dokumentet. |
| [set_ImageHeight](./set_imageheight/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Sättare för [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageHeight](./get_imageheight/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Anger strömmen som mail merge‑motorn ska läsa en bild från. |
| [set_ImageStream](./set_imagestream/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [set_ImageWidth](./set_imagewidth/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Sättare för [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth](./get_imagewidth/). |
| [set_Shape](./set_shape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Sättare för [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape](./get_shape/). |
| static [Type](./type/)() |  |
## Anmärkningar


Detta händelse inträffar under mail merge när ett bild‑mail merge‑fält påträffas i dokumentet. Du kan svara på denna händelse genom att returnera ett filnamn, en ström eller ett **Image**‑objekt till mail merge‑motorn så att det infogas i dokumentet.

Det finns tre egenskaper tillgängliga [ImageFileName](./get_imagefilename/), [ImageStream](./get_imagestream/) och [Image](./get_image/) för att ange var bilden ska hämtas från. Ställ in endast en av dessa egenskaper.

För att infoga ett bild‑mail merge‑fält i ett dokument i Word, välj kommandot Infoga/Fält, välj sedan MergeField och skriv Image:MyFieldName.

## Se även

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
