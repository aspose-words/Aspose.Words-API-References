---
title: "Aspose::Words::Shading class"
linktitle: "Shading"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Shading class. Bir nesne için gölgelendirme özelliklerini içerir. Daha fazla bilgi için C++'ta belgeler makalesini ziyaret edin."
type: docs
weight: 60000
url: /tr/cpp/aspose.words/shading/
---
## Shading class


Bir nesne için gölgelendirme özniteliklerini içerir. Daha fazla bilgi edinmek için, [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) dokümantasyon makalesini ziyaret edin.

```cpp
class Shading : public Aspose::Words::InternableComplexAttr,
                public Aspose::Words::IComplexAttr
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Nesneden gölgelendirmeyi kaldırır. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Shading\>\&) | Belirtilen [Shading](./) değerinin mevcut [Shading](./) ile eşit olup olmadığını belirler. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Belirtilen nesnenin mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [get_BackgroundPatternColor](./get_backgroundpatterncolor/)() | [Shading](./) nesnesinin arka planına uygulanan rengi alır veya ayarlar. |
| [get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/)() | Bu [Shading](./) nesnesiyle ilişkili uygulanan renk şemasındaki arka plan desen tema rengini alır veya ayarlar. |
| [get_BackgroundTintAndShade](./get_backgroundtintandshade/)() | Arka plan tema rengini aydınlatan veya karartan bir double değerini alır veya ayarlar. |
| [get_ForegroundPatternColor](./get_foregroundpatterncolor/)() | Ön planına uygulanan rengi alır veya ayarlar [Shading](./) nesnesi için. |
| [get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/)() | Uygulanan renk şemasında bu [Shading](./) nesnesiyle ilişkili ön plan desen tema rengini alır veya ayarlar. |
| [get_ForegroundTintAndShade](./get_foregroundtintandshade/)() | Ön plan tema rengini açan veya karartan bir çift değer alır veya ayarlar. |
| [get_Texture](./get_texture/)() | Gölgelendirme dokusunu alır veya ayarlar. |
| [GetHashCode](./gethashcode/)() const override | Bu tip için bir karma (hash) işlevi olarak hizmet verir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackgroundPatternColor](./set_backgroundpatterncolor/)(System::Drawing::Color) | [Aspose::Words::Shading::get_BackgroundPatternColor](./get_backgroundpatterncolor/) için ayarlayıcı. |
| [set_BackgroundPatternThemeColor](./set_backgroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | [Aspose::Words::Shading::get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/) için ayarlayıcı. |
| [set_BackgroundTintAndShade](./set_backgroundtintandshade/)(double) | [Aspose::Words::Shading::get_BackgroundTintAndShade](./get_backgroundtintandshade/) için ayarlayıcı. |
| [set_ForegroundPatternColor](./set_foregroundpatterncolor/)(System::Drawing::Color) | [Aspose::Words::Shading::get_ForegroundPatternColor](./get_foregroundpatterncolor/) için ayarlayıcı. |
| [set_ForegroundPatternThemeColor](./set_foregroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | [Aspose::Words::Shading::get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/) için ayarlayıcı. |
| [set_ForegroundTintAndShade](./set_foregroundtintandshade/)(double) | [Aspose::Words::Shading::get_ForegroundTintAndShade](./get_foregroundtintandshade/) için ayarlayıcı. |
| [set_Texture](./set_texture/)(Aspose::Words::TextureIndex) | [Aspose::Words::Shading::get_Texture](./get_texture/) için ayarlayıcı. |
| static [Type](./type/)() |  |

## Örnekler



Bir tablo oluştururken kenarlık ve gölgelendirme renginin nasıl uygulanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir tablo başlatın ve kenarlıkları için varsayılan renk/kalınlığı ayarlayın.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Farklı arka plan renklerine sahip iki hücreli bir satır oluşturun.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Arka plan renklerini devre dışı bırakmak için hücre biçimlendirmesini sıfırla
// Yapıcı tarafından oluşturulan tüm yeni hücreler için özel bir kenarlık kalınlığı ayarlayın,
// sonra ikinci bir satır oluşturun.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


Metni kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```

## Ayrıca Bakınız

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
