---
title: "Aspose::Words::CompositeNode::GetChild metodu"
linktitle: "GetChild"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::CompositeNode::GetChild metodu. C++'da belirtilen tipe uyan N'inci çocuk düğümü döndürür."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/compositenode/getchild/
---
## CompositeNode::GetChild method


Belirtilen tipe uyan N'inci çocuk düğümünü döndürür.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::GetChild(Aspose::Words::NodeType nodeType, int32_t index, bool isDeep)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Çocuk düğümünün tipini belirtir. |
| index | int32_t | Seçilecek çocuk düğümünün sıfır tabanlı indeksi. Negatif indeksler de izin verilir ve sondan erişimi gösterir, yani -1 son düğüm anlamına gelir. |
| isDeep | bool | **true** tüm çocuk düğümlerinden özyinelemeli olarak seçmek için; **false** yalnızca doğrudan çocuklar arasında seçmek için. Daha fazla bilgi için açıklamalara bakın. |

### ReturnValue

Kriterlere uyan çocuk düğüm veya eşleşen düğüm bulunamazsa **null**.
## Açıklamalar


İndeks aralık dışındaysa, **null** döndürülür.

## Örnekler



Bir birleşik düğümün alt düğüm koleksiyonunda nasıl gezileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bu belgenin ilk paragrafına iki koşu ve bir şekil alt düğüm olarak ekle.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Not: 'CustomNodeId' bir çıktı dosyasına kaydedilmez ve yalnızca düğüm ömrü boyunca vardır.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Paragrafın doğrudan alt eleman koleksiyonunda yineleme yapın,
// ve içinde bulduğumuz tüm run'ları veya şekilleri yazdırın.
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```

## Ayrıca Bakınız

* Class [Node](../../node/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
