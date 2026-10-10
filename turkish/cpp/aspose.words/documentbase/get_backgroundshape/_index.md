---
title: "Aspose::Words::DocumentBase::get_BackgroundShape yöntemi"
linktitle: "get_BackgroundShape"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBase::get_BackgroundShape yöntemi. Belgenin arka plan şekline erişir veya onu ayarlar. C++'da null olabilir."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/documentbase/get_backgroundshape/
---
## DocumentBase::get_BackgroundShape method


Belgenin arka plan şekli alınır veya ayarlanır. **null** olabilir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBase::get_BackgroundShape() const
```

## Açıklamalar


Microsoft Word, bir belgenin arka plan şekli olarak yalnızca [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) özelliği [Rectangle](../../../aspose.words.drawing/shapetype/) olan şekle izin verir.

Microsoft Word, bir arka plan şeklinin yalnızca dolgu özelliklerini destekler. Diğer tüm özellikler yok sayılır.

Bu özelliği null olmayan bir değere ayarlamak, aynı zamanda [DisplayBackgroundShape](../../../aspose.words.settings/viewoptions/get_displaybackgroundshape/) özelliğini **true** yapar.

## Örnekler



Bir belgenin her sayfası için arka plan şeklinin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_TRUE(System::TestTools::IsNull(doc->get_BackgroundShape()));

// Arka plan olarak kullanabileceğimiz tek şekil türü bir dikdörtgendir.
auto shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);

// Bu şekli sayfa arka planı olarak kullanmanın iki yolu vardır.
// 1 -  Düz bir renk:
shapeRectangle->set_FillColor(System::Drawing::Color::get_LightBlue());
doc->set_BackgroundShape(shapeRectangle);

doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.FlatColor.docx");

// 2 -  Bir resim:
shapeRectangle = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shapeRectangle->get_ImageData()->SetImage(get_ImageDir() + u"Transparent background logo.png");

// Resmin görünümünü ayarlayarak, filigran olarak daha uygun hale getirin.
shapeRectangle->get_ImageData()->set_Contrast(0.2);
shapeRectangle->get_ImageData()->set_Brightness(0.7);

doc->set_BackgroundShape(shapeRectangle);

ASSERT_TRUE(doc->get_BackgroundShape()->get_HasImage());

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
saveOptions->set_CacheBackgroundGraphics(false);

// Microsoft Word, arka plan olarak resim içeren şekilleri desteklemez,
// ancak bu arka planları .pdf gibi diğer kaydetme formatlarında hâlâ görebiliriz.
doc->Save(get_ArtifactsDir() + u"DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
