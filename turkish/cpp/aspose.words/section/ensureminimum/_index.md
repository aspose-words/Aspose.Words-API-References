---
title: "Aspose::Words::Section::EnsureMinimum yöntemi"
linktitle: "EnsureMinimum"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Section::EnsureMinimum yöntemi. Bölümün C++'ta bir Paragraph içeren Body'si olduğundan emin olur."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/section/ensureminimum/
---
## Section::EnsureMinimum method


Bölümün [Body](../get_body/) içinde bir [Paragraph](../../paragraph/) olduğundan emin olur.

```cpp
void Aspose::Words::Section::EnsureMinimum()
```


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

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
