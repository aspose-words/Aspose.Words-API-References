---
title: "Aspose::Words::MailMerging::FieldMergingArgs class"
linktitle: "FieldMergingArgs"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MailMerging::FieldMergingArgs sınıfı. MergeField olayı için veri sağlar. Daha fazla bilgi için C++'taki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class


**MergeField** olayı için veri sağlar. Daha fazla bilgi için, [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) dokümantasyon makalesini ziyaret edin.

```cpp
class FieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Birleştirmenin gerçekleştirildiği [Document](../fieldmergingargsbase/get_document/) nesnesini döndürür. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Belgede belirtildiği gibi birleştirme alanının adını alır. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Geçerli birleştirme alanını temsil eden nesneyi alır. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Veri kaynağındaki birleştirme alanının adını alır. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Veri kaynağından alanın değerini alır. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Birleştirilen kaydın sıfır tabanlı dizinini alır. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Geçerli birleştirme işlemi için veri tablosunun adını alır; ad mevcut değilse boş dize döndürür. |
| [get_Text](./get_text/)() const | Geçerli birleştirme alanı için belgeye eklenecek metni alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Veri kaynağından alanın değerini ayarlar. |
| [set_Text](./set_text/)(const System::String\&) | [Aspose::Words::MailMerging::FieldMergingArgs::get_Text](./get_text/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


**MergeField** olayı, belge içinde basit bir birleştirme alanıyle karşılaşıldığında birleştirme sırasında gerçekleşir. Bu olaya yanıt vererek, birleştirme motorunun belgeye eklemesi için metin döndürebilirsiniz.

## Ayrıca Bakınız

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
