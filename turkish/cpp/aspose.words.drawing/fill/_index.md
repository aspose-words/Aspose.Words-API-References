---
title: "Aspose::Words::Drawing::Fill class"
linktitle: "Fill"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Fill sınıfı. Bir nesne için dolgu biçimlendirmesini temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.drawing/fill/
---
## Fill class


Bir nesne için dolgu biçimlendirmesini temsil eder. Daha fazla bilgi için, [Working with Graphic Elements](https://docs.aspose.com/words/cpp/working-with-graphic-elements/) dokümantasyon makalesini ziyaret edin.

```cpp
class Fill : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Dolgu için arka plan rengini temsil eden bir Color nesnesini alır veya ayarlar. |
| [get_BackThemeColor](./get_backthemecolor/)() | Dolgu için arka plan rengini temsil eden bir ThemeColor nesnesini alır veya ayarlar. |
| [get_BackTintAndShade](./get_backtintandshade/)() | Arka plan rengini açan veya karartan bir double değerini alır veya ayarlar. |
| [get_BaseForeColor](./get_baseforecolor/)() | Herhangi bir değiştirici olmadan dolgu için temel ön plan rengini temsil eden bir Color nesnesini alır. |
| [get_Color](./get_color/)() | Dolgu için ön plan rengini temsil eden bir Color nesnesini alır veya ayarlar. |
| [get_FillType](./get_filltype/)() | Bir dolgu tipini alır. |
| [get_ForeColor](./get_forecolor/)() | Dolgu için ön plan rengini temsil eden bir Color nesnesini alır. |
| [get_ForeThemeColor](./get_forethemecolor/)() | Dolgu için ön plan rengini temsil eden bir ThemeColor nesnesini alır veya ayarlar. |
| [get_ForeTintAndShade](./get_foretintandshade/)() | Ön plan rengini açan veya karartan bir double değerini alır veya ayarlar. |
| [get_GradientAngle](./get_gradientangle/)() | Gradyan dolgunun açısını alır veya ayarlar. |
| [get_GradientStops](./get_gradientstops/)() | Dolgu için bir [GradientStop](../gradientstop/) nesneleri koleksiyonunu alır. |
| [get_GradientStyle](./get_gradientstyle/)() | Dolgu için gradyan stilini [GradientStyle](../gradientstyle/) alır. |
| [get_GradientVariant](./get_gradientvariant/)() | Dolgu için gradyan varyantını [GradientVariant](../gradientvariant/) alır. |
| [get_ImageBytes](./get_imagebytes/)() | Dolgu dokusunun veya deseninin ham baytlarını alır. |
| [get_Opacity](./get_opacity/)() | Belirtilen dolgunun opaklık derecesini 0.0 (şeffaf) ile 1.0 (opak) arasında bir değer olarak alır veya ayarlar. |
| [get_Pattern](./get_pattern/)() | Dolgu için bir [PatternType](../patterntype/) alır. |
| [get_PresetTexture](./get_presettexture/)() | Dolgu için bir [PresetTexture](../presettexture/) alır. |
| [get_RotateWithObject](./get_rotatewithobject/)() | Dolgunun belirtilen nesneyle birlikte döndürülüp döndürülmediğini alır. |
| [get_TextureAlignment](./get_texturealignment/)() | Döşeme doku dolgu için hizalamayı alır veya ayarlar. |
| [get_Transparency](./get_transparency/)() | Belirtilen dolgunun şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak alır veya ayarlar. |
| [get_Visible](./get_visible/)() | Bu örneğe uygulanan biçimlendirme görünürse **true** değerini alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OneColorGradient](./onecolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Belirtilen dolguyu tek renkli bir gradyana ayarlar. |
| [OneColorGradient](./onecolorgradient/)(System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) | Belirtilen dolguyu belirtilen rengi kullanarak tek renkli bir gradyana ayarlar. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType) | Belirtilen dolguyu bir desene ayarlar. |
| [Patterned](./patterned/)(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) | Belirtilen dolguyu bir desene ayarlar. |
| [PresetTextured](./presettextured/)(Aspose::Words::Drawing::PresetTexture) | Dolgu önceden ayarlanmış bir dokuya ayarlar. |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Drawing::Fill::get_BackColor](./get_backcolor/). |
| [set_BackThemeColor](./set_backthemecolor/)(Aspose::Words::Themes::ThemeColor) | Ayarlayıcı [Aspose::Words::Drawing::Fill::get_BackThemeColor](./get_backthemecolor/). |
| [set_BackTintAndShade](./set_backtintandshade/)(double) | Ayarlayıcı [Aspose::Words::Drawing::Fill::get_BackTintAndShade](./get_backtintandshade/). |
| [set_Color](./set_color/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Drawing::Fill::get_Color](./get_color/). |
| [set_ForeColor](./set_forecolor/)(System::Drawing::Color) | Dolgu için ön plan rengini temsil eden bir Color nesnesi ayarlar. |
| [set_ForeThemeColor](./set_forethemecolor/)(Aspose::Words::Themes::ThemeColor) | Ayarlayıcı [Aspose::Words::Drawing::Fill::get_ForeThemeColor](./get_forethemecolor/). |
| [set_ForeTintAndShade](./set_foretintandshade/)(double) | Ayarlayıcı [Aspose::Words::Drawing::Fill::get_ForeTintAndShade](./get_foretintandshade/). |
| [set_GradientAngle](./set_gradientangle/)(double) | Ayarlayıcı [Aspose::Words::Drawing::Fill::get_GradientAngle](./get_gradientangle/). |
| [set_Opacity](./set_opacity/)(double) | Ayarlayıcı [Aspose::Words::Drawing::Fill::get_Opacity](./get_opacity/). |
| [set_RotateWithObject](./set_rotatewithobject/)(bool) | Dolgunun belirtilen nesneyle birlikte dönüp dönmeyeceğini ayarlar. |
| [set_TextureAlignment](./set_texturealignment/)(Aspose::Words::Drawing::TextureAlignment) | Ayarlayıcı [Aspose::Words::Drawing::Fill::get_TextureAlignment](./get_texturealignment/). |
| [set_Transparency](./set_transparency/)(double) | Ayarlayıcı [Aspose::Words::Drawing::Fill::get_Transparency](./get_transparency/). |
| [set_Visible](./set_visible/)(bool) | Bu örneğe uygulanan biçimlendirme görünürse **true** olan değeri ayarlar. |
| [SetImage](./setimage/)(const System::String\&) | Dolgu tipini tek bir görüntüye değiştirir. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Dolgu tipini tek bir görüntüye değiştirir. |
| [SetImage](./setimage/)(const System::ArrayPtr\<uint8_t\>\&) | Dolgu tipini tek bir görüntüye değiştirir. |
| [Solid](./solid/)() | Dolgu tek renkli bir renge ayarlar. |
| [Solid](./solid/)(System::Drawing::Color) | Dolgu belirtilen tek renkli bir renge ayarlar. |
| [TwoColorGradient](./twocolorgradient/)(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Belirtilen dolguyu iki renkli bir degradeye ayarlar. |
| [TwoColorGradient](./twocolorgradient/)(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) | Belirtilen dolguyu iki renkli bir degradeye ayarlar. |
| static [Type](./type/)() |  |
## Açıklamalar


Bir nesnenin dolgu özelliklerine erişmek için [Fill](../shapebase/get_fill/) veya [Fill](../../aspose.words/font/get_fill/) özelliğini kullanın. [Fill](./) sınıfının örneklerini doğrudan oluşturmazsınız.

## Örnekler



Bir şekli katı bir renk ile doldurmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Biraz metin yazın ve ardından onu yüzen bir şekille kapatın.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Use the "StrokeColor" özelliğini kullanarak şeklin dış kenarının rengini ayarlayın.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Use the "FillColor" özelliğini kullanarak şeklin iç bölgesinin rengini ayarlayın.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// "Opacity" özelliği, rengin 0-1 ölçeğinde ne kadar şeffaf olduğunu belirler,
// 1 tamamen opak, 0 ise görünmez olur.
// Şekil dolgu varsayılan olarak tamamen opaktır, bu yüzden bu şeklin üstünde olduğu metni göremiyoruz.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Şekil dolgu renginin opaklığını daha düşük bir değere ayarlayın, böylece altındaki metni görebiliriz.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
