---
title: "Aspose::Words::Drawing::Fill::TwoColorGradient yöntemi"
linktitle: "TwoColorGradient"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Fill::TwoColorGradient yöntemi. Belirtilen doldurmayı C++'ta iki renkli bir degradeye ayarlar."
type: docs
weight: 44000
url: /tr/cpp/aspose.words.drawing/fill/twocolorgradient/
---
## Fill::TwoColorGradient(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) method


Belirtilen dolguyu iki renkli bir degradeye ayarlar.

```cpp
void Aspose::Words::Drawing::Fill::TwoColorGradient(Aspose::Words::Drawing::GradientStyle style, Aspose::Words::Drawing::GradientVariant variant)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| style | Aspose::Words::Drawing::GradientStyle | Degrade stili [GradientStyle](../../gradientstyle/). |
| variant | Aspose::Words::Drawing::GradientVariant | Degrade varyantı [GradientVariant](../../gradientvariant/) |

## Örnekler



Bir şekli degrade ile doldurmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Şekle, degrade doldurmanın ForeColor özelliği ile tek renkli bir degrade doldurma uygula.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Şekle iki renkli degrade doldurma uygula.
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// Degrade doldurmanın BackColor özelliğini değiştir.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Şunu unutmayın: "GradientAngle" değişiklikleri "GradientStyle.FromCorner/GradientStyle.FromCenter" için
// gradient doldurma hiçbir etki göstermez, yalnızca doğrusal degrade için çalışır.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// Şekli DML kullanarak tanımlamak istiyorsanız uyumluluk seçeneğini kullanın, "GradientStyle" elde etmek için,
// "GradientVariant" ve "GradientAngle" özellikleri belge kaydedildikten sonra.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## Ayrıca Bakınız

* Enum [GradientStyle](../../gradientstyle/)
* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::TwoColorGradient(System::Drawing::Color, System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant) method


Belirtilen dolguyu iki renkli bir degradeye ayarlar.

```cpp
void Aspose::Words::Drawing::Fill::TwoColorGradient(System::Drawing::Color color1, System::Drawing::Color color2, Aspose::Words::Drawing::GradientStyle style, Aspose::Words::Drawing::GradientVariant variant)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| color1 | System::Drawing::Color | Degradi oluşturmak için ilk renk. |
| color2 | System::Drawing::Color | Degradi oluşturmak için ikinci renk. |
| style | Aspose::Words::Drawing::GradientStyle | Degrade stili [GradientStyle](../../gradientstyle/). |
| variant | Aspose::Words::Drawing::GradientVariant | Degrade varyantı [GradientVariant](../../gradientvariant/) |

## Örnekler



Bir şekli degrade ile doldurmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Şekle, degrade doldurmanın ForeColor özelliği ile tek renkli bir degrade doldurma uygula.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Şekle iki renkli degrade doldurma uygula.
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// Degrade doldurmanın BackColor özelliğini değiştir.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Şunu unutmayın: "GradientAngle" değişiklikleri "GradientStyle.FromCorner/GradientStyle.FromCenter" için
// gradient doldurma hiçbir etki göstermez, yalnızca doğrusal degrade için çalışır.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// Şekli DML kullanarak tanımlamak istiyorsanız uyumluluk seçeneğini kullanın, "GradientStyle" elde etmek için,
// "GradientVariant" ve "GradientAngle" özellikleri belge kaydedildikten sonra.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## Ayrıca Bakınız

* Enum [GradientStyle](../../gradientstyle/)
* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
