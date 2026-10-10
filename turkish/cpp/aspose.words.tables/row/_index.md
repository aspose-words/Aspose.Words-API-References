---
title: "Aspose::Words::Tables::Row class"
linktitle: "Row"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Row sınıfı. Bir tablo satırını temsil eder. Daha fazla bilgi için C++ belgelerindeki makaleyi ziyaret edin."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.tables/row/
---
## Row class


Bir tablo satırını temsil eder. Daha fazla bilgi edinmek için [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) dokümantasyon makalesini ziyaret edin.

```cpp
class Row : public Aspose::Words::CompositeNode,
            public Aspose::Words::IRowAttrSource,
            public Aspose::Words::Revisions::ITrackableNode
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Satırın sonunu ziyaret etmek için bir ziyaretçiyi kabul eder. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Satırın başlangıcını ziyaret etmek için bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [EnsureMinimum](./ensureminimum/)() | Eğer [Row](./) hücre içermiyorsa, bir [Cell](../cell/) oluşturur ve ekler. |
| [get_Cells](./get_cells/)() | Satırın [Cell](../cell/) alt düğümlerine tipli erişim sağlar. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_FirstCell](./get_firstcell/)() | Satırdaki ilk [Cell](../cell/) döndürür. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_Hidden](./get_hidden/)() | Bu satırın gizli olup olmadığını gösteren bir bayrağı alır veya ayarlar. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_IsFirstRow](./get_isfirstrow/)() | Bir tabloda bu ilk satırsa doğru; aksi takdirde yanlış. |
| [get_IsLastRow](./get_islastrow/)() | Bir tabloda bu son satırsa doğru; aksi takdirde yanlış. |
| [get_LastCell](./get_lastcell/)() | Satırdaki son [Cell](../cell/) döndürür. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextRow](./get_nextrow/)() | Sonraki [Row](./) düğümünü alır. |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | [Row](../../aspose.words/nodetype/) döndürür. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_ParentTable](./get_parenttable/)() | Satırın doğrudan üst tabloyu döndürür. |
| [get_PreviousRow](./get_previousrow/)() | Önceki [Row](./) düğümünü alır. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Bu düğümde bulunan belge bölümünü temsil eden bir [Range](../../aspose.words/range/) nesnesi döndürür. |
| [get_RowFormat](./get_rowformat/)() | Satırın biçimlendirme özelliklerine erişim sağlar. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../../aspose.words/nodetype/) ilk atasını alır. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Belirtilen tipe uyan N'inci çocuk düğümünü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| [GetText](./gettext/)() override | Bu satırdaki tüm hücrelerin metnini, satır sonu karakteri dahil olmak üzere alır. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Belirtilen alt düğümün alt düğüm dizisindeki indeksini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Bir düğüm türü enum değerini kullanıcı dostu bir dizeye dönüştüren yardımcı bir yöntem. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendisini üst düğümden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Geçerli düğümün tüm [SmartTag](../../aspose.words.markup/smarttag/) alt düğümlerini kaldırır. |
| [Row](./row/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | [Row](./) sınıfının yeni bir örneğini başlatır. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | XPath ifadesiyle eşleşen bir düğüm listesi seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | XPath ifadesiyle eşleşen ilk [Node](../../aspose.words/node/) öğesini seçer. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) için ayarlayıcı. |
| [set_Hidden](./set_hidden/)(bool) | [Aspose::Words::Tables::Row::get_Hidden](./get_hidden/) için ayarlayıcı. |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


[Row](./) can only be a child of a [Table](../table/).

[Row](./) can contain one or more [Cell](../cell/) nodes.

Geçerli bir minimal satırın en az bir [Cell](../cell/) içermesi gerekir.

## Örnekler



Bir tablo oluşturmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Tablolar satırları içerir, satırlar hücreleri içerir, hücreler paragraf içerebilir
// koşular, şekiller ve hatta diğer tablolar gibi tipik öğelerle.
// Bir tablo üzerinde "EnsureMinimum" yöntemini çağırmak, şunun sağlanmasını garantiler
// tablonun en az bir satır, bir hücre ve bir paragrafı vardır.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Metni tablonun ilk satırındaki ilk hücreye ekleyin.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```


Belgedeki tüm tabloları dolaşmayı ve her hücrenin içeriğini yazdırmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Bir satır koleksiyonunda "ToArray" metodunu kullanarak onu bir diziye kopyalayabiliriz.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Bir hücre koleksiyonunda "ToArray" metodunu kullanarak onu bir diziye kopyalayabiliriz.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(Aspose::Words::SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
```

## Ayrıca Bakınız

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
