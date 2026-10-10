---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs class"
linktitle: "ImageFieldMergingArgs"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs sınıfı. ImageFieldMerging() olayı için veri sağlar. Daha fazla bilgi için C++'taki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class


[ImageFieldMerging()](../ifieldmergingcallback/imagefieldmerging/) olayı için veri sağlar. Daha fazla bilgi için [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) belge makalesini ziyaret edin.

```cpp
class ImageFieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Birleştirmenin gerçekleştirildiği [Document](../fieldmergingargsbase/get_document/) nesnesini döndürür. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Belgede belirtildiği gibi birleştirme alanının adını alır. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Geçerli birleştirme alanını temsil eden nesneyi alır. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Veri kaynağındaki birleştirme alanının adını alır. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Veri kaynağından alanın değerini alır. |
| [get_Image](./get_image/)() const | Posta birleştirme motorunun belgeye eklemesi gereken resmi belirtir. |
| [get_ImageFileName](./get_imagefilename/)() const | Posta birleştirme motorunun belgeye eklemesi gereken resmin dosya adını ayarlar. |
| [get_ImageHeight](./get_imageheight/)() const | Belgeye eklenecek resmin yüksekliğini belirtir. |
| [get_ImageStream](./get_imagestream/)() const | Posta birleştirme motorunun bir resim okuması için akışı belirtir. |
| [get_ImageWidth](./get_imagewidth/)() const | Belgeye eklenecek resmin genişliğini belirtir. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Birleştirilen kaydın sıfır tabanlı dizinini alır. |
| [get_Shape](./get_shape/)() const | Posta birleştirme motorunun belgeye eklemesi gereken şekli belirtir. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Geçerli birleştirme işlemi için veri tablosunun adını alır; ad mevcut değilse boş dize döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Veri kaynağından alanın değerini ayarlar. |
| [set_Image](./set_image/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Posta birleştirme motorunun belgeye eklemesi gereken resmi belirtir. |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Posta birleştirme motorunun belgeye eklemesi gereken resmin dosya adını ayarlar. |
| [set_ImageHeight](./set_imageheight/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageHeight](./get_imageheight/) için ayarlayıcı. |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Posta birleştirme motorunun bir resim okuması için akışı belirtir. |
| [set_ImageStream](./set_imagestream/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [set_ImageWidth](./set_imagewidth/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth](./get_imagewidth/) için ayarlayıcı. |
| [set_Shape](./set_shape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape](./get_shape/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


Bu olay, belge içinde bir resim posta birleştirme alanı ile karşılaşıldığında posta birleştirme sırasında gerçekleşir. Bu olaya yanıt vererek bir dosya adı, akış veya **Image** nesnesi döndürebilir ve posta birleştirme motorunun belgeye eklemesini sağlayabilirsiniz.

Resmin nereden alınacağını belirtmek için üç özellik mevcuttur: [ImageFileName](./get_imagefilename/), [ImageStream](./get_imagestream/) ve [Image](./get_image/). Bu özelliklerden yalnızca birini ayarlayın.

Word'de bir belgeye resim posta birleştirme alanı eklemek için Ekle/Alan komutunu seçin, ardından BirleştirmeAlanı'nı seçin ve Image:MyFieldName yazın.

## Ayrıca Bakınız

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
