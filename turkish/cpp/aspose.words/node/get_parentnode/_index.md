---
title: "Aspose::Words::Node::get_ParentNode yöntemi"
linktitle: "get_ParentNode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Node::get_ParentNode yöntemi. Bu düğümün hemen üst düğümünü C++'da alır."
type: docs
weight: 10000
url: /tr/cpp/aspose.words/node/get_parentnode/
---
## Node::get_ParentNode method


Bu düğümün doğrudan ebeveynini alır.

```cpp
System::SharedPtr<Aspose::Words::CompositeNode> Aspose::Words::Node::get_ParentNode()
```

## Açıklamalar


Bir düğüm yeni oluşturulmuş ve henüz ağaca eklenmemişse ya da ağaçtan kaldırılmışsa, üst düğüm **null** olur.

## Örnekler



Bir düğümün üst düğümüne nasıl erişileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Belgenin ilk paragrafına bir çocuk Run düğümü ekleyin.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Paragraf, run düğümünün üst düğümüdür. Bu soy ağacını izleyebiliriz
// belge düğümüne kadar, ki bu belge düğüm ağacının köküdür.
ASPOSE_ASSERT_EQ(para, run->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection(), doc->get_FirstSection()->get_Body()->get_ParentNode());
ASPOSE_ASSERT_EQ(doc, doc->get_FirstSection()->get_ParentNode());
```


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

* Class [CompositeNode](../../compositenode/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
