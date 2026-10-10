---
title: "Aspose::Words::NodeType enum"
linktitle: "NodeType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeType enum. C++'da bir Word belge düğümünün tipini belirtir."
type: docs
weight: 102000
url: /tr/cpp/aspose.words/nodetype/
---
## NodeType enum


Bir Word belge düğümünün türünü belirtir.

```cpp
enum class NodeType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Herhangi | 0 | Tüm düğüm tiplerini gösterir. Tüm alt öğeleri seçmeye izin verir. |
| Document | 1 | Belge ağacının kökü olarak, tüm Word belgesine erişim sağlayan bir [Document](../document/) nesnesi. Bir [Document](../document/) düğümü [Section](../section/) düğümlerine sahip olabilir. |
| Section | 2 | Word belgesindeki bir bölüme karşılık gelen bir [Section](../section/) nesnesi. Bir [Section](../section/) düğümü [Body](../body/) ve [HeaderFooter](../headerfooter/) düğümlerine sahip olabilir. |
| Body | 3 | Bir bölüm içinde belirli bir başlık veya altbilgi metnini içeren bir [HeaderFooter](../headerfooter/) nesnesi. Bir [HeaderFooter](../headerfooter/) düğümü [Paragraph](../paragraph/) ve [Table](../../aspose.words.tables/table/) düğümlerine sahip olabilir. |
| HeaderFooter | 4 | Word belgesindeki bir tabloyu temsil eden bir [Table](../../aspose.words.tables/table/) nesnesi. Bir [Table](../../aspose.words.tables/table/) düğümü [Row](../../aspose.words.tables/row/) düğümlerine sahip olabilir. |
| Table | 5 | Bir tablonun satırı. Bir [Row](../../aspose.words.tables/row/) düğümü [Cell](../../aspose.words.tables/cell/) düğümlerine sahip olabilir. |
| Row | 6 | Bir tablo satırının hücresi. Bir [Cell](../../aspose.words.tables/cell/) düğümü [Paragraph](../paragraph/) ve [Table](../../aspose.words.tables/table/) düğümlerine sahip olabilir. |
| Cell | 7 | Bir metin paragrafı. Bir [Paragraph](../paragraph/) düğümü, satır içi seviyedeki öğeler olan [Run](../run/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [Footnote](../../aspose.words.notes/footnote/), [Comment](../comment/), [SpecialChar](../specialchar/), ayrıca [BookmarkStart](../bookmarkstart/) ve [BookmarkEnd](../bookmarkend/) öğelerinin bir kapsayıcısıdır. |
| Paragraph | 8 | Bir yer imi işaretleyicisinin başlangıcı. |
| BookmarkStart | 9 | BookmarkEnd |
| Bir yer imi işaretleyicisinin sonu. | 10 | EditableRangeStart |
| Düzenlenebilir bir aralığın başlangıcı. | 11 | EditableRangeEnd |
| Düzenlenebilir bir aralığın sonu. | 12 | MoveFromRangeStart |
| Bir MoveFrom aralığının başlangıcı. | 13 | MoveFromRangeEnd |
| Bir MoveFrom aralığının sonu. | 14 | MoveToRangeStart |
| Bir MoveTo aralığının başlangıcı. | 15 | MoveTo aralığının bir başlangıcı. |
| MoveToRangeEnd | 16 | Bir MoveTo aralığının sonu. |
| GroupShape | 17 | Şekiller, görüntüler, OLE nesneleri veya diğer grup şekillerinin bir grubu. Bir [GroupShape](../../aspose.words.drawing/groupshape/) düğümü diğer [Shape](../../aspose.words.drawing/shape/) ve [GroupShape](../../aspose.words.drawing/groupshape/) düğümlerini içerebilir. |
| Shape | 18 | Bir çizim nesnesi, örneğin bir OfficeArt şekli, görüntü veya bir OLE nesnesi. Bir [Shape](../../aspose.words.drawing/shape/) düğümü [Paragraph](../paragraph/) ve [Table](../../aspose.words.tables/table/) düğümlerini içerebilir. |
| Comment | 19 | Word belgesindeki bir yorum. Bir [Comment](../comment/) düğümü [Paragraph](../paragraph/) ve [Table](../../aspose.words.tables/table/) düğümlerine sahip olabilir. |
| Footnote | 20 | Word belgesindeki bir dipnot veya sonnot. Bir [Footnote](../../aspose.words.notes/footnote/) düğümü [Paragraph](../paragraph/) ve [Table](../../aspose.words.tables/table/) düğümlerine sahip olabilir. |
| Run | 21 | Bir metin parçası. |
| FieldStart | 22 | Word alanının başlangıcını belirten özel bir karakter. |
| FieldSeparator | 23 | Alan kodunu alan sonucundan ayıran özel bir karakter. |
| FieldEnd | 24 | Word alanının sonunu belirten özel bir karakter. |
| FormField | 25 | Bir form alanı. |
| SpecialChar | 26 | Daha spesifik özel karakter türlerinden biri olmayan bir özel karakter. |
| SmartTag | 27 | Bir paragrafta bir veya daha fazla satır içi yapı (koşular, görüntüler, alanlar, vb.) etrafında bir akıllı etiket. |
| StructuredDocumentTag | 28 | Müşteriye özgü bilgileri ve bunların sunum biçimini tanımlamayı sağlar. |
| StructuredDocumentTagRangeStart | 29 | **ranged** yapılandırılmış belge etiketinin çok bölümlü içeriği kabul eden başlangıcı. |
| StructuredDocumentTagRangeEnd | 30 | **ranged** yapılandırılmış belge etiketinin çok bölümlü içeriği kabul eden sonu. |
| GlossaryDocument | 31 | Ana belge içinde bir sözlük belgesi. |
| BuildingBlock | 32 | Bir sözlük belgesi içinde bir yapı taşı (ör. sözlük belge girişi). |
| CommentRangeStart | 33 | Yorumlanmış bir aralığın başlangıcını temsil eden bir işaretçi düğüm. |
| CommentRangeEnd | 34 | Yorumlanmış bir aralığın sonunu temsil eden bir işaretçi düğüm. |
| OfficeMath | 35 | Bir Office [Math](../../aspose.words.math/) nesnesi. Denklem, fonksiyon, matris veya diğer matematiksel nesnelerden biri olabilir. Matematiksel nesnelerin bir koleksiyonu olabilir ve ayrıca metin akışları gibi bazı matematik dışı nesneler de içerebilir. |
| SubDocument | 36 | Başka bir belgeye bağlantı olan bir alt belge düğümü. |
| System | 37 | [Aspose.Words](../) tarafından dahili kullanım için ayrılmıştır. |
| Null | 38 | [Aspose.Words](../) tarafından dahili kullanım için ayrılmıştır. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
