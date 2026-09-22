---
title: "Aspose::Words::Range sınıfı"
linktitle: "Aralık"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Range sınıfı. Bir belgede kesintisiz bir alanı temsil eder. Daha fazla bilgi için C++ belgelerindeki makaleyi ziyaret edin."
type: docs
weight: 51000
url: /tr/cpp/aspose.words/range/
---
## Range class


Bir belgede kesintisiz bir alanı temsil eder. Daha fazla bilgi edinmek için, [Working with Ranges](https://docs.aspose.com/words/cpp/working-with-ranges/) dokümantasyon makalesini ziyaret edin.

```cpp
class Range : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Delete](./delete/)() | Aralıktaki tüm karakterleri siler. |
| [get_Bookmarks](./get_bookmarks/)() | Aralıktaki tüm yer imlerini temsil eden bir [Bookmarks](./get_bookmarks/) koleksiyonu döndürür. |
| [get_Fields](./get_fields/)() | Aralıktaki tüm alanları temsil eden bir [Fields](./get_fields/) koleksiyonu döndürür. |
| [get_FormFields](./get_formfields/)() | Aralıktaki tüm form alanlarını temsil eden bir [FormFields](./get_formfields/) koleksiyonu döndürür. |
| [get_Revisions](./get_revisions/)() | Bu aralıkta mevcut olan revizyonların (izlenen değişiklikler) bir koleksiyonunu alır. |
| [get_StructuredDocumentTags](./get_structureddocumenttags/)() | Aralıktaki tüm yapılandırılmış belge etiketlerini temsil eden bir [StructuredDocumentTags](./get_structureddocumenttags/) koleksiyonu döndürür. |
| [get_Text](./get_text/)() | Aralığın metnini alır. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Bu aralıktaki [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) öğelerinin [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) değerlerini, alan kodlarında bulunan alan tipleriyle eşleşecek şekilde değiştirir. |
| [Replace](./replace/)(const System::String\&, const System::String\&) | Belirtilen karakter dizesi deseninin tüm görünümlerini bir değiştirme dizesiyle değiştirir. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Düzenli ifade ile belirtilen karakter deseninin tüm görünümlerini başka bir dizeyle değiştirir. |
| [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Belirtilen karakter dizesi deseninin tüm görünümlerini bir değiştirme dizesiyle değiştirir. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Düzenli ifade ile belirtilen karakter deseninin tüm görünümlerini başka bir dizeyle değiştirir. |
| [ToDocument](./todocument/)() | Aralığı içeren yeni, tam oluşturulmuş bir belge oluşturur. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Bu aralıktaki alanların bağlantısını kaldırır. |
| [UpdateFields](./updatefields/)() | Bu aralıktaki belge alanlarının değerlerini günceller. |
## Açıklamalar


Belge, düğümlerin bir ağacıyla temsil edilir ve düğümler ağacla çalışmak için işlemler sağlar, ancak belge bir kesintisiz metin dizisi olarak ele alındığında bazı işlemler daha kolay yapılır.

[Range](./) is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

[Range](./) does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.

## Örnekler



Bir aralığın kapsadığı tüm düğümlerin metin içeriğini nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
