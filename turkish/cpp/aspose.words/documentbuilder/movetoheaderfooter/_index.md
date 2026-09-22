---
title: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter method"
linktitle: "MoveToHeaderFooter"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter yöntemi. İmleci C++'ta geçerli bölümdeki bir başlık ya da altbilginin başlangıcına taşır."
type: docs
weight: 57000
url: /tr/cpp/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder::MoveToHeaderFooter method


İmleci geçerli bölümdeki bir üst bilgi ya da alt bilginin başına taşır.

```cpp
void Aspose::Words::DocumentBuilder::MoveToHeaderFooter(Aspose::Words::HeaderFooterType headerFooterType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Taşınacak başlık ya da altbilgiyi belirtir. |
## Açıklamalar


İmleci bir başlık ya da altbilgiye taşıdıktan sonra, [DocumentBuilder](../) yöntemlerinin geri kalanını kullanarak başlık ya da altbilginin içeriğini değiştirebilirsiniz.

İlk sayfa için farklı başlık ve altbilgi oluşturmak istiyorsanız, [DifferentFirstPageHeaderFooter](../../pagesetup/get_differentfirstpageheaderfooter/) ayarını yapmanız gerekir.

Çift ve tek sayfalar için farklı başlık ve altbilgi oluşturmak istiyorsanız, [OddAndEvenPagesHeaderFooter](../../pagesetup/get_oddandevenpagesheaderfooter/) ayarını yapmanız gerekir.

[MoveToSection()](../movetosection/) yöntemini kullanarak başlıktan çıkıp ana metne geçebilirsiniz.

## Örnekler



Bir görüntünün nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Görüntüyü başlığa ekleyin, böylece her sayfada görünür.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Görüntüyü sayfanın ortasına yerleştirin.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```

## Ayrıca Bakınız

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
