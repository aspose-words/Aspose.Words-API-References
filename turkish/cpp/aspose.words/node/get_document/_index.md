---
title: "Aspose::Words::Node::get_Document yöntemi"
linktitle: "get_Document"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Node::get_Document yöntemi. C++'ta bu düğümün ait olduğu belgeyi alır."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/node/get_document/
---
## Node::get_Document method


Bu düğümün ait olduğu belgeyi alır.

```cpp
virtual System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Node::get_Document() const
```

## Açıklamalar


Düğüm, yeni oluşturulmuş ve henüz ağaca eklenmemiş olsa bile ya da ağaçtan kaldırılmış olsa bile her zaman bir belgeye aittir.

## Örnekler



Bir düğüm oluşturmayı ve sahip belgeyi ayarlamayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Bu paragrafı henüz herhangi bir birleşik düğüme çocuk olarak eklemedik.
ASSERT_TRUE(System::TestTools::IsNull(para->get_ParentNode()));

// Bir düğüm, başka bir birleşik düğümün uygun bir çocuk düğüm türü ise,
// Bunu yalnızca her iki düğümün aynı sahip belgeye sahip olması durumunda çocuk olarak ekleyebiliriz.
// Sahip belge, düğümün yapıcı metoduna gönderdiğimiz belgedir.
// Bu paragrafı belgeye eklemedik, bu yüzden belge metnini içermez.
ASPOSE_ASSERT_EQ(para->get_Document(), doc);
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());

// Belge bu paragrafın sahib olduğu için, paragraf içeriğine belgenin stillerinden birini uygulayabiliriz.
para->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));

// Bu düğümü belgeye ekleyin ve ardından içeriğini doğrulayın.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [DocumentBase](../../documentbase/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
