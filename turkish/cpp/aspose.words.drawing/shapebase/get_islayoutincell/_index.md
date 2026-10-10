---
title: "Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell yöntemi"
linktitle: "get_IsLayoutInCell"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell yöntemi. C++'de şeklin bir tablo içinde mi yoksa dışında mı görüntülendiğini gösteren bir bayrağı alır veya ayarlar."
type: docs
weight: 32000
url: /tr/cpp/aspose.words.drawing/shapebase/get_islayoutincell/
---
## ShapeBase::get_IsLayoutInCell method


Şeklin bir tablo içinde mi yoksa dışında mı görüntülendiğini gösteren bayrağı alır veya ayarlar.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell()
```

## Açıklamalar


Varsayılan değer **true**'dır.

Yalnızca üst düzey şekiller için etkilidir, [WrapType](../get_wraptype/) özelliği [Inline](../../../aspose.words/inline/) dışındaki bir değere ayarlandığında.

## Örnekler



Bir şeklin tablo hücresinde nasıl görüntüleneceğini belirlemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(10);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

table->set_Style(tableStyle);

builder->MoveTo(table->get_FirstRow()->get_FirstCell()->get_FirstParagraph());

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 50, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);

// Şekli hücrenin paragrafı içinde satır içi bir öğe olarak görüntülemek için "IsLayoutInCell" özelliğini "true" olarak ayarlayın.
// Şeklin konumunu belirleyecek koordinat başlangıcı, şeklin hücresinin sol üst köşesi olacaktır.
// Hücreyi yeniden boyutlandırırsak, şekil hücrenin sol üst köşesinden başlayarak aynı konumu korumak için hareket eder.
// Şekli bağımsız bir yüzen şekil olarak görüntülemek için "IsLayoutInCell" özelliğini "false" olarak ayarlayın.
// Şeklin konumunu belirleyecek koordinat başlangıcı, sayfanın sol üst köşesi olacaktır,
// ve şekil hücresinin herhangi bir yeniden boyutlandırılmasına yanıt vermeyecektir.
shape->set_IsLayoutInCell(isLayoutInCell);

// "IsLayoutInCell" özelliğini yalnızca yüzen şekillere uygulayabiliriz.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

doc->Save(get_ArtifactsDir() + u"Shape.LayoutInTableCell.docx");
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
