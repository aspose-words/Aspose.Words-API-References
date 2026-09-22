---
title: "Aspose::Words::TableStyle sınıfı"
linktitle: "TableStyle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TableStyle sınıfı. Bir tablo stilini temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 67000
url: /tr/cpp/aspose.words/tablestyle/
---
## TableStyle class


Bir tablo stilini temsil eder. Daha fazla bilgi edinmek için, [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) belgeler makalesini ziyaret edin.

```cpp
class TableStyle : public Aspose::Words::Style,
                   public Aspose::Words::ICellAttrSource,
                   public Aspose::Words::IRowAttrSource,
                   public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Equals](../style/equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Belirtilen stil ile karşılaştırır. Styles Istds yalnızca yerleşik stiller için karşılaştırılır. Stil varsayılanları karşılaştırmaya dahil edilmez. Temel stil, bağlı stil ve sonraki paragraf stili özyinelemeli olarak karşılaştırılır. |
| [get_Aliases](../style/get_aliases/)() | Bu stilin tüm takma adlarını alır. Stil takma ada sahip değilse boş bir dize dizisi döndürülür. |
| [get_Alignment](./get_alignment/)() | Tablo stili için hizalamayı belirtir. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | Bir tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin verilip verilmediğini gösteren bayrağı alır veya ayarlar. |
| [get_AutomaticallyUpdate](../style/get_automaticallyupdate/)() const | Bu stilin uygun değere göre otomatik olarak yeniden tanımlanıp tanımlanmayacağını belirtir. |
| [get_BaseStyleName](../style/get_basestylename/)() | Bu stilin dayandığı stilin adını alır/ayar. |
| [get_Borders](./get_borders/)() | Stil için varsayılan hücre kenarlıklarının koleksiyonunu alır. |
| [get_BottomPadding](./get_bottompadding/)() | Tablo hücrelerinin içeriğinin altına eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [get_BuiltIn](../style/get_builtin/)() | Bu stil MS Word'deki yerleşik stillerden biri ise doğru. |
| [get_CellSpacing](./get_cellspacing/)() | Hücreler arasındaki boşluk miktarını (puan cinsinden) alır veya ayarlar. |
| [get_ColumnStripe](./get_columnstripe/)() | Stil tek/çift sütun şeritlemesi belirttiğinde şeritlemeye dahil edilecek sütun sayısını alır veya ayarlar. |
| [get_ConditionalStyles](./get_conditionalstyles/)() | Bu tablo stili için tanımlanabilecek koşullu stillerin koleksiyonu. |
| [get_Document](../style/get_document/)() | Sahip belgeyi alır. |
| [get_Font](../style/get_font/)() | Stilin karakter biçimlendirmesini alır. |
| [get_IsHeading](../style/get_isheading/)() | Stil yerleşik Başlık stillerinden biri olduğunda doğru. |
| [get_IsQuickStyle](../style/get_isquickstyle/)() const | Bu stilin MS Word UI içinde Hızlı [Style](../style/) galerisinde gösterilip gösterilmeyeceğini belirtir. |
| [get_LeftIndent](./get_leftindent/)() | Bir tablonun sol girintisini temsil eden değeri alır veya ayarlar. |
| [get_LeftPadding](./get_leftpadding/)() | Tablo hücrelerinin içeriğinin soluna eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [get_LinkedStyleName](../style/get_linkedstylename/)() | Bu stile bağlı olan [Style](../style/) adını alır/ayarlar. Bağlı stil yoksa boş dize döndürür. |
| [get_List](../style/get_list/)() | Bu liste stilinin biçimlendirmesini tanımlayan listeyi alır. |
| [get_ListFormat](../style/get_listformat/)() | Bir paragraf stilinin liste biçimlendirme özelliklerine erişim sağlar. |
| [get_Locked](../style/get_locked/)() const | Bu stilin kilitli olup olmadığını belirtir. |
| [get_Name](../style/get_name/)() const | Stilin adını alır veya ayarlar. |
| [get_NextParagraphStyleName](../style/get_nextparagraphstylename/)() | Belirtilen stil ile biçimlendirilmiş bir paragraftan sonra eklenen yeni paragrafa otomatik olarak uygulanacak stilin adını alır/ayar. |
| [get_ParagraphFormat](../style/get_paragraphformat/)() | Stilin paragraf biçimlendirmesini alır. |
| [get_Priority](../style/get_priority/)() const | Stiller görev bölmesinde stilleri sıralama önceliğini temsil eden tam sayı değerini alır/ayar. |
| [get_RightPadding](./get_rightpadding/)() | Tablo hücrelerinin içeriğinin sağına eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [get_RowStripe](./get_rowstripe/)() | Stil tek/çift satır şeritlemesi belirttiğinde şeritlemeye dahil edilecek satır sayısını alır veya ayarlar. |
| [get_SemiHidden](../style/get_semihidden/)() const | Stilin Styles galerisinden ve Styles görev bölmesinden gizlenip gizlenmediğini alır/ayarlar. |
| [get_Shading](./get_shading/)() | Tablo hücreleri için gölgelendirme biçimlendirmesine referans veren bir [Shading](../shading/) nesnesi alır. |
| [get_StyleIdentifier](../style/get_styleidentifier/)() const | Yerel bağımsız bir yerleşik stil için stil tanımlayıcısını alır. |
| [get_Styles](../style/get_styles/)() const | Bu stilin ait olduğu stil koleksiyonunu alır. |
| [get_TopPadding](./get_toppadding/)() | Tablo hücrelerinin içeriğinin üstüne eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [get_Type](../style/get_type/)() const | Stil tipini (paragraf veya karakter) alır. |
| [get_UnhideWhenUsed](../style/get_unhidewhenused/)() const | Geçerli belgede kullanılan stilin Styles galerisinden ve Styles görev bölmesinden gizlenip gizlenmediğini alır/ayarlar. Stil galerisinde gösterilmesi gerektiğinde doğru (true) olur. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Hücreler için dikey hizalamayı belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../style/remove/)() | Belirtilen stili belgeden kaldırır. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Tables::TableAlignment) | [Aspose::Words::TableStyle::get_Alignment](./get_alignment/) için ayarlayıcı. |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | [Aspose::Words::TableStyle::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/) için ayarlayıcı. |
| [set_AutomaticallyUpdate](../style/set_automaticallyupdate/)(bool) | [Aspose::Words::Style::get_AutomaticallyUpdate](../style/get_automaticallyupdate/) için ayarlayıcı. |
| [set_BaseStyleName](../style/set_basestylename/)(const System::String\&) | [Aspose::Words::Style::get_BaseStyleName](../style/get_basestylename/) için ayarlayıcı. |
| [set_BottomPadding](./set_bottompadding/)(double) | [Aspose::Words::TableStyle::get_BottomPadding](./get_bottompadding/) için ayarlayıcı. |
| [set_CellSpacing](./set_cellspacing/)(double) | [Aspose::Words::TableStyle::get_CellSpacing](./get_cellspacing/) için ayarlayıcı. |
| [set_ColumnStripe](./set_columnstripe/)(int32_t) | [Aspose::Words::TableStyle::get_ColumnStripe](./get_columnstripe/) için ayarlayıcı. |
| [set_IsQuickStyle](../style/set_isquickstyle/)(bool) | [Aspose::Words::Style::get_IsQuickStyle](../style/get_isquickstyle/) için ayarlayıcı. |
| [set_LeftIndent](./set_leftindent/)(double) | [Aspose::Words::TableStyle::get_LeftIndent](./get_leftindent/) için ayarlayıcı. |
| [set_LeftPadding](./set_leftpadding/)(double) | [Aspose::Words::TableStyle::get_LeftPadding](./get_leftpadding/) için ayarlayıcı |
| [set_LinkedStyleName](../style/set_linkedstylename/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Style::get_LinkedStyleName](../style/get_linkedstylename/). |
| [set_Locked](../style/set_locked/)(bool) | Ayarlayıcı [Aspose::Words::Style::get_Locked](../style/get_locked/). |
| [set_Name](../style/set_name/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Style::get_Name](../style/get_name/). |
| [set_NextParagraphStyleName](../style/set_nextparagraphstylename/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Style::get_NextParagraphStyleName](../style/get_nextparagraphstylename/). |
| [set_Priority](../style/set_priority/)(int32_t) | Ayarlayıcı [Aspose::Words::Style::get_Priority](../style/get_priority/). |
| [set_RightPadding](./set_rightpadding/)(double) | Ayarlayıcı [Aspose::Words::TableStyle::get_RightPadding](./get_rightpadding/). |
| [set_RowStripe](./set_rowstripe/)(int32_t) | Ayarlayıcı [Aspose::Words::TableStyle::get_RowStripe](./get_rowstripe/). |
| [set_SemiHidden](../style/set_semihidden/)(bool) | Ayarlayıcı [Aspose::Words::Style::get_SemiHidden](../style/get_semihidden/). |
| [set_TopPadding](./set_toppadding/)(double) | Ayarlayıcı [Aspose::Words::TableStyle::get_TopPadding](./get_toppadding/). |
| [set_UnhideWhenUsed](../style/set_unhidewhenused/)(bool) | Ayarlayıcı [Aspose::Words::Style::get_UnhideWhenUsed](../style/get_unhidewhenused/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Ayarlayıcı [Aspose::Words::TableStyle::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |

## Örnekler



Tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// Bir tablonun stil özelliklerini ayarlamak, tablonun kendi özelliklerini etkileyebilir.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Ayrıca Bakınız

* Class [Style](../style/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
