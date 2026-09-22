---
title: "Aspose::Words::Tables::Table sınıfı"
linktitle: "Table"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table sınıfı. Bir Word belgesindeki tabloyu temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.tables/table/
---
## Table class


Bir Word belgesindeki tabloyu temsil eder. Daha fazla bilgi edinmek için [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) dokümantasyon makalesini ziyaret edin.

```cpp
class Table : public Aspose::Words::CompositeNode
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Bir ziyaretçiyi kabul eder. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Tablonun sonunu ziyaret etmek için bir ziyaretçi kabul eder. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Tablonun başlangıcını ziyaret etmek için bir ziyaretçi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AutoFit](./autofit/)(Aspose::Words::Tables::AutoFitBehavior) | Belirtilen otomatik sığdırma davranışına göre tabloyu ve hücreleri yeniden boyutlandırır. |
| [ClearBorders](./clearborders/)() | Bu tablodaki tüm tablo ve hücre kenarlıklarını kaldırır. |
| [ClearShading](./clearshading/)() | Tablodaki tüm gölgelendirmeleri kaldırır. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [ConvertToHorizontallyMergedCells](./converttohorizontallymergedcells/)() | Hücreleri genişliklerine göre yatay birleştirilmiş olanları, [HorizontalMerge](../cellformat/get_horizontalmerge/) ile birleştirilmiş hücrelere dönüştürür. |
| [EnsureMinimum](./ensureminimum/)() | Tablonun satırı yoksa, bir [Row](../row/) oluşturur ve ekler. |
| [get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/)() | Tablo özellikleri tarafından belirtilen mutlak yatay yüzen tablo konumunu, puan cinsinden alır veya ayarlar. Varsayılan değer 0'dır. |
| [get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/)() | Tablo özellikleri tarafından belirtilen mutlak dikey yüzen tablo konumunu, puan cinsinden alır veya ayarlar. Varsayılan değer 0'dır. |
| [get_Alignment](./get_alignment/)() | Bir satır içi tablonun belgede nasıl hizalanacağını belirtir. |
| [get_AllowAutoFit](./get_allowautofit/)() | Microsoft Word ve Aspose.Words'in bir tablodaki hücreleri içeriklerine sığacak şekilde otomatik olarak yeniden boyutlandırmasına izin verir. |
| [get_AllowCellSpacing](./get_allowcellspacing/)() | “Hücreler arasında boşluk bırakılmasına izin ver” seçeneğini alır veya ayarlar. |
| [get_AllowOverlap](./get_allowoverlap/)() | Bir yüzen tablonun, belgede diğer yüzen nesnelerin görüntülendiğinde kapsamının üstüne gelmesine izin verip vermeyeceğini alır. Varsayılan değer **true**'dır. |
| [get_Bidi](./get_bidi/)() | Bunun sağdan sola bir tablo olup olmadığını alır veya ayarlar. |
| [get_BottomPadding](./get_bottompadding/)() | Hücre içeriklerinin altına eklenecek boşluk miktarını (puan cinsinden) alır veya ayarlar. |
| [get_CellSpacing](./get_cellspacing/)() | Hücreler arasındaki boşluk miktarını (puan cinsinden) alır veya ayarlar. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Bu düğümün doğrudan çocuk sayısını alır. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Özel düğüm tanımlayıcısını belirtir. |
| [get_Description](./get_description/)() | Bu tablonun açıklamasını alır veya ayarlar. Tablo içinde bulunan bilginin alternatif bir metin temsili sağlar. |
| [get_DistanceBottom](./get_distancebottom/)() | Tablonun altı ile çevresindeki metin arasındaki mesafeyi, puan cinsinden alır veya ayarlar. |
| [get_DistanceLeft](./get_distanceleft/)() | Tablonun solu ile çevresindeki metin arasındaki mesafeyi, puan cinsinden alır veya ayarlar. |
| [get_DistanceRight](./get_distanceright/)() | Tablonun sağı ile çevresindeki metin arasındaki mesafeyi, puan cinsinden alır veya ayarlar. |
| [get_DistanceTop](./get_distancetop/)() | Tablonun üstü ile çevresindeki metin arasındaki mesafeyi, puan cinsinden alır veya ayarlar. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Bu düğümün ait olduğu belgeyi alır. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Düğümün ilk çocuğunu alır. |
| [get_FirstRow](./get_firstrow/)() | Tablodaki ilk [Row](../row/) düğümünü döndürür. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Bu düğümün herhangi bir çocuğu varsa **true** döndürür. |
| [get_HorizontalAnchor](./get_horizontalanchor/)() | Yüzen tablonun yatay konumlandırmasının hesaplanacağı temel nesneyi alır. Varsayılan değer [Column](../../aspose.words.drawing/relativehorizontalposition/)'dır. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Bu düğümün çocuk düğümleri olabileceği için **true** döndürür. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Düğümün son çocuğunu alır. |
| [get_LastRow](./get_lastrow/)() | Tablodaki son [Row](../row/) düğümünü döndürür. |
| [get_LeftIndent](./get_leftindent/)() | Tablonun sol girintisini temsil eden değeri alır veya ayarlar. |
| [get_LeftPadding](./get_leftpadding/)() | Hücre içeriklerinin soluna eklenecek boşluk miktarını (puan cinsinden) alır veya ayarlar. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Bu düğümü hemen izleyen düğümü alır. |
| [get_NodeType](./get_nodetype/)() const override | Döndürür [Table](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Bu düğümün doğrudan ebeveynini alır. |
| [get_PreferredWidth](./get_preferredwidth/)() | Tablonun tercih edilen genişliğini alır veya ayarlar. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Bu düğümden hemen önce gelen düğümü alır. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Bu düğümde bulunan belge bölümünü temsil eden bir [Range](../../aspose.words/range/) nesnesi döndürür. |
| [get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/)() | Yüzen tablonun göreceli yatay hizalamasını alır veya ayarlar. |
| [get_RelativeVerticalAlignment](./get_relativeverticalalignment/)() | Yüzen tablonun göreceli dikey hizalamasını alır veya ayarlar. |
| [get_RightPadding](./get_rightpadding/)() | Hücre içeriklerinin sağına eklenecek boşluk miktarını (puan cinsinden) alır veya ayarlar. |
| [get_Rows](./get_rows/)() | Tablonun satırlarına tipli erişim sağlar. |
| [get_Style](./get_style/)() | Bu tabloya uygulanan tablo stilini alır veya ayarlar. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Bu tabloya uygulanan tablo stilinin bölge bağımsız stil tanımlayıcısını alır veya ayarlar. |
| [get_StyleName](./get_stylename/)() | Bu tabloya uygulanan tablo stilinin adını alır veya ayarlar. |
| [get_StyleOptions](./get_styleoptions/)() | Bir tablo stilinin bu tabloya nasıl uygulandığını belirten bit bayraklarını alır veya ayarlar. |
| [get_TextWrapping](./get_textwrapping/)() | Tablo için [TextWrapping](./get_textwrapping/) alır veya ayarlar. |
| [get_Title](./get_title/)() | Bu tablonun başlığını alır veya ayarlar. Tablo içinde bulunan bilgilerin alternatif bir metin temsili sağlar. |
| [get_TopPadding](./get_toppadding/)() | Hücre içeriklerinin üstüne eklenecek boşluk miktarını (puan cinsinden) alır veya ayarlar. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Yüzen tablonun dikey konumlandırmasının hesaplanacağı temel nesneyi alır. Varsayılan değer [Margin](../../aspose.words.drawing/relativeverticalposition/)'dır. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Belirtilen [NodeType](../../aspose.words/nodetype/) ilk atasını alır. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Belirtilen tipe uyan N'inci çocuk düğümünü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Bu düğümün alt düğümleri üzerinde foreach tarzı yinelemeyi destekler. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
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
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | XPath ifadesiyle eşleşen bir düğüm listesi seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | XPath ifadesiyle eşleşen ilk [Node](../../aspose.words/node/) öğesini seçer. |
| [set_AbsoluteHorizontalDistance](./set_absolutehorizontaldistance/)(double) | [Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance](./get_absolutehorizontaldistance/) için ayarlayıcı. |
| [set_AbsoluteVerticalDistance](./set_absoluteverticaldistance/)(double) | [Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance](./get_absoluteverticaldistance/) için ayarlayıcı. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | [Aspose::Words::Tables::Table::get_Alignment](./get_alignment/) için ayarlayıcı. |
| [set_AllowAutoFit](./set_allowautofit/)(bool) | [Aspose::Words::Tables::Table::get_AllowAutoFit](./get_allowautofit/) için ayarlayıcı. |
| [set_AllowCellSpacing](./set_allowcellspacing/)(bool) | [Aspose::Words::Tables::Table::get_AllowCellSpacing](./get_allowcellspacing/) için ayarlayıcı. |
| [set_Bidi](./set_bidi/)(bool) | [Aspose::Words::Tables::Table::get_Bidi](./get_bidi/) için ayarlayıcı. |
| [set_BottomPadding](./set_bottompadding/)(double) | [Aspose::Words::Tables::Table::get_BottomPadding](./get_bottompadding/) için ayarlayıcı. |
| [set_CellSpacing](./set_cellspacing/)(double) | [Aspose::Words::Tables::Table::get_CellSpacing](./get_cellspacing/) için ayarlayıcı. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) için ayarlayıcı. |
| [set_Description](./set_description/)(const System::String\&) | [Aspose::Words::Tables::Table::get_Description](./get_description/) için ayarlayıcı. |
| [set_DistanceBottom](./set_distancebottom/)(double) | [Aspose::Words::Tables::Table::get_DistanceBottom](./get_distancebottom/) için ayarlayıcı. |
| [set_DistanceLeft](./set_distanceleft/)(double) | [Aspose::Words::Tables::Table::get_DistanceLeft](./get_distanceleft/) için ayarlayıcı. |
| [set_DistanceRight](./set_distanceright/)(double) | [Aspose::Words::Tables::Table::get_DistanceRight](./get_distanceright/) için ayarlayıcı. |
| [set_DistanceTop](./set_distancetop/)(double) | [Aspose::Words::Tables::Table::get_DistanceTop](./get_distancetop/) için ayarlayıcı. |
| [set_HorizontalAnchor](./set_horizontalanchor/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | [Aspose::Words::Tables::Table::get_HorizontalAnchor](./get_horizontalanchor/) için ayarlayıcı. |
| [set_LeftIndent](./set_leftindent/)(double) | [Aspose::Words::Tables::Table::get_LeftIndent](./get_leftindent/) için ayarlayıcı. |
| [set_LeftPadding](./set_leftpadding/)(double) | [Aspose::Words::Tables::Table::get_LeftPadding](./get_leftpadding/) için ayarlayıcı. |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | [Aspose::Words::Tables::Table::get_PreferredWidth](./get_preferredwidth/) için ayarlayıcı. |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalAlignment](./set_relativehorizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | [Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment](./get_relativehorizontalalignment/) için ayarlayıcı. |
| [set_RelativeVerticalAlignment](./set_relativeverticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | [Aspose::Words::Tables::Table::get_RelativeVerticalAlignment](./get_relativeverticalalignment/) için ayarlayıcı. |
| [set_RightPadding](./set_rightpadding/)(double) | [Aspose::Words::Tables::Table::get_RightPadding](./get_rightpadding/) için ayarlayıcı. |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | [Aspose::Words::Tables::Table::get_Style](./get_style/) için ayarlayıcı. |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | [Aspose::Words::Tables::Table::get_StyleIdentifier](./get_styleidentifier/) için ayarlayıcı. |
| [set_StyleName](./set_stylename/)(const System::String\&) | [Aspose::Words::Tables::Table::get_StyleName](./get_stylename/) için ayarlayıcı. |
| [set_StyleOptions](./set_styleoptions/)(Aspose::Words::Tables::TableStyleOptions) | [Aspose::Words::Tables::Table::get_StyleOptions](./get_styleoptions/) için ayarlayıcı. |
| [set_TextWrapping](./set_textwrapping/)(Aspose::Words::Tables::TextWrapping) | [Aspose::Words::Tables::Table::get_TextWrapping](./get_textwrapping/) için ayarlayıcı. |
| [set_Title](./set_title/)(const System::String\&) | [Aspose::Words::Tables::Table::get_Title](./get_title/) için ayarlayıcı. |
| [set_TopPadding](./set_toppadding/)(double) | [Aspose::Words::Tables::Table::get_TopPadding](./get_toppadding/) için ayarlayıcı. |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::RelativeVerticalPosition) | [Aspose::Words::Tables::Table::get_VerticalAnchor](./get_verticalanchor/) için ayarlayıcı. |
| [SetBorder](./setborder/)(Aspose::Words::BorderType, Aspose::Words::LineStyle, double, System::Drawing::Color, bool) | Belirtilen tablo kenarlığını belirtilen çizgi stiline, genişliğe ve renge ayarlar. |
| [SetBorders](./setborders/)(Aspose::Words::LineStyle, double, System::Drawing::Color) | Tüm tablo kenarlıklarını belirtilen çizgi stiline, genişliğe ve renge ayarlar. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetShading](./setshading/)(Aspose::Words::TextureIndex, System::Drawing::Color, System::Drawing::Color) | Tüm tablo üzerinde gölgelendirmeyi belirtilen değerlere ayarlar. |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [Table](./table/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Yeni bir [Table](./) sınıfının örneğini başlatır. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Düğümün içeriğini belirtilen formatta bir dizeye dışa aktarır. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| static [Type](./type/)() |  |
## Açıklamalar


[Table](./) is a block-level node and can be a child of classes derived from [Story](../../aspose.words/story/) or [InlineStory](../../aspose.words/inlinestory/).

[Table](./) can contain one or more [Row](../row/) nodes.

Geçerli bir minimal tablo en az bir [Row](../row/) içermelidir.

## Örnekler



Biçimlendirilmiş 2x2 tablo nasıl oluşturulur gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// Tablo oluşturulurken, belge oluşturucu mevcut RowFormat/CellFormat özellik değerlerini uygular
// imlecin bulunduğu mevcut satır/hücreye ve oluşturduğu yeni satır/hücrelere.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Daha önce eklenen satır ve hücreler, oluşturucunun biçimlendirme değişikliklerinden geriye dönük olarak etkilenmez.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```


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
