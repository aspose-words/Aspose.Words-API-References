---
title: "Aspose::Words::Drawing::ImageData::get_CropTop yöntemi"
linktitle: "get_CropTop"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ImageData::get_CropTop yöntemi. C++'da resmin üst taraftan kaldırılma oranını tanımlar."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.drawing/imagedata/get_croptop/
---
## ImageData::get_CropTop method


Defines the fraction of picture removal from the top side.

```cpp
double Aspose::Words::Drawing::ImageData::get_CropTop()
```

## Açıklamalar


Kırpma miktarı -1.0 ile 1.0 arasında değişebilir. Varsayılan değer 0'dır. 1 değeri, hiçbir resim gösterilmeyeceği anlamına gelir. Negatif değerler, kırpılan kenardan resmin içe doğru sıkıştırılmasına neden olur (resim ile kırpılan kenar arasındaki boşluk şeklin dolgu rengiyle doldurulur). 1'den küçük pozitif değerler, kalan resmin şekle sığacak şekilde gerilmesine yol açar.

Varsayılan değer 0'dır.

## Örnekler



Bir şeklin görüntü verisini nasıl düzenleyeceğini gösterir.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");
auto sourceShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

auto dstDoc = System::MakeObject<Aspose::Words::Document>();

// Kaynak belgeden bir şekil içe aktar ve bunu ilk paragrafın sonuna ekle.
auto importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

// İçe aktarılan şekil bir görüntü içerir. Görüntünün özelliklerine ve ham verilerine ImageData nesnesi aracılığıyla erişebiliriz.
System::SharedPtr<Aspose::Words::Drawing::ImageData> imageData = importedShape->get_ImageData();
imageData->set_Title(u"Imported Image");

ASSERT_TRUE(imageData->get_HasImage());

// Bir görüntünün kenarlıkları yoksa, ImageData nesnesi kenar rengi olarak boş tanımlayacaktır.
ASSERT_EQ(4, imageData->get_Borders()->get_Count());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, imageData->get_Borders()->idx_get(0)->get_Color());

// Bu görüntü, yerel dosya sistemindeki başka bir şekle veya görüntü dosyasına bağlanmaz.
ASSERT_FALSE(imageData->get_IsLink());
ASSERT_FALSE(imageData->get_IsLinkOnly());

// "Brightness" ve "Contrast" özellikleri görüntü parlaklığını ve kontrastını tanımlar
// 0-1 ölçeğinde, varsayılan değer 0.5'tir.
imageData->set_Brightness(0.8);
imageData->set_Contrast(1.0);

// Yukarıdaki parlaklık ve kontrast değerleri, çok beyaz bir görüntü oluşturdu.
// ChromaKey özelliğiyle bir renk seçerek, örneğin beyazı, şeffaflıkla değiştirebiliriz.
imageData->set_ChromaKey(System::Drawing::Color::get_White());

// Kaynak şekli tekrar içe aktar ve görüntüyü tek renkli (monochrome) olarak ayarla.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_GrayScale(true);

// Kaynak şekli tekrar içe aktar, üçüncü bir görüntü oluştur ve onu BiLevel olarak ayarla.
// BiLevel, her pikseli orijinal renge daha yakın olan siyah veya beyaz olarak ayarlar.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_BiLevel(true);

// Kırpma, 0-1 ölçeğinde belirlenir. Bir kenarı 0.3 oranında kırpmak
// kırpılan kenarda görüntünün %30'unu kırpar.
importedShape->get_ImageData()->set_CropBottom(0.3);
importedShape->get_ImageData()->set_CropLeft(0.3);
importedShape->get_ImageData()->set_CropTop(0.3);
importedShape->get_ImageData()->set_CropRight(0.3);

dstDoc->Save(get_ArtifactsDir() + u"Drawing.ImageData.docx");
```

## Ayrıca Bakınız

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
