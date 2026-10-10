---
title: "Aspose::Words::Document::EnsureMinimum yöntemi"
linktitle: "EnsureMinimum"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::EnsureMinimum yöntemi. Belge hiçbir bölüm içermiyorsa, C++'ta bir paragraf içeren bir bölüm oluşturur."
type: docs
weight: 10000
url: /tr/cpp/aspose.words/document/ensureminimum/
---
## Document::EnsureMinimum method


Belge hiçbir bölüm içermiyorsa, bir paragraf içeren bir bölüm oluşturur.

```cpp
void Aspose::Words::Document::EnsureMinimum()
```


## Örnekler



Bir belgenin içeriğini düzenlemek için gereken minimum düğüm setine sahip olmasını nasıl sağlayacağınızı gösterir.
```cpp
// Yeni oluşturulan bir belge bir alt Bölüm içerir; bu Bölüm bir alt Gövde ve bir alt Paragraf içerir.
// Belgenin gövde içeriğini, o paragraf içine Run'lar veya satır içi Şekiller gibi düğümler ekleyerek düzenleyebiliriz.
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASPOSE_ASSERT_EQ(doc, nodes->idx_get(0)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(0), nodes->idx_get(1)->get_ParentNode());

ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());
ASPOSE_ASSERT_EQ(nodes->idx_get(1), nodes->idx_get(2)->get_ParentNode());

// Bu, belgeyi düzenleyebilmek için ihtiyaç duyduğumuz minimum düğüm setidir.
// Bunlardan herhangi birini kaldırırsak belgeyi artık düzenleyemeyeceğiz.
doc->RemoveAllChildren();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Belgenin en az bu üç düğüme sahip olduğundan emin olmak ve tekrar düzenleyebilmek için bu yöntemi çağırın.
doc->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Section, nodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, nodes->idx_get(1)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, nodes->idx_get(2)->get_NodeType());

(System::ExplicitCast<Aspose::Words::Paragraph>(nodes->idx_get(2)))->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
