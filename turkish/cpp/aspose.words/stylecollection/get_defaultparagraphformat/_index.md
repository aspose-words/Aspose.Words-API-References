---
title: "Aspose::Words::StyleCollection::get_DefaultParagraphFormat method"
linktitle: "get_DefaultParagraphFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::StyleCollection::get_DefaultParagraphFormat method. C++'ta belge varsayılan paragraf biçimlendirmesini alır."
type: docs
weight: 7000
url: /tr/cpp/aspose.words/stylecollection/get_defaultparagraphformat/
---
## StyleCollection::get_DefaultParagraphFormat method


Belgenin varsayılan paragraf biçimlendirmesini alır.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::StyleCollection::get_DefaultParagraphFormat()
```

## Açıklamalar


Not: Belge geneli varsayılanlar Microsoft Word 2007'de tanıtıldı ve yalnızca OOXML formatlarında ([Docx](../../loadformat/)) tam olarak desteklenir. Daha eski belge formatları belge varsayılan paragraf biçimlendirmesini desteklemez.

## Örnekler



Bir belgenin stil koleksiyonuna bir [Style](../../style/) nasıl eklenir gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Bu koleksiyona daha sonra ekleyebileceğimiz yeni stiller için varsayılan parametreleri ayarlayın.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Eğer "StyleType.Paragraph" stilini eklersek, koleksiyon değerlerini uygular
// "DefaultParagraphFormat" özelliğini stilin "ParagraphFormat" özelliğine.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Bir stil ekleyin ve ardından varsayılan ayarları içerdiğini doğrulayın.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../../paragraphformat/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
