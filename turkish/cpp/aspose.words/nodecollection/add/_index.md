---
title: "Aspose::Words::NodeCollection::Add method"
linktitle: "Add"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeCollection::Add yöntemi. C++'da bir düğümü koleksiyonun sonuna ekler."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/nodecollection/add/
---
## NodeCollection::Add method


Bir düğümü koleksiyonun sonuna ekler.

```cpp
void Aspose::Words::NodeCollection::Add(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| düğüm | const System::SharedPtr\<Aspose::Words::Node\>\& | Koleksiyonun sonuna eklenecek düğüm. |
## Açıklamalar


Düğüm, koleksiyonun oluşturulduğu düğüm nesnesine alt öğe olarak eklenir.

Eğer eklenen düğüm başka bir belgeden oluşturulmuşsa, düğümü geçerli belgeye aktarmak için [ImportNode()](../) kullanmalısınız. İçe aktarılan düğüm daha sonra geçerli belgeye eklenebilir.

## Örnekler



Yeni bir bölüm düğümünü düzenleme için nasıl hazırlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Boş bir belge bir bölümle gelir, bu bölümün bir body'si vardır ve bu body'nin bir paragraph'ı vardır.
// Bu belgeye içerik eklemek için o paragrafın içine text runs, shapes veya tables gibi öğeler ekleyebiliriz.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// Böyle bir yeni bölüm eklersek, bir body'si veya başka herhangi bir alt düğümü olmayacaktır.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// "EnsureMinimum" yöntemini çalıştırarak bu bölüme bir body ve bir paragraf ekleyin, böylece düzenlemeye başlayabilirsiniz.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
