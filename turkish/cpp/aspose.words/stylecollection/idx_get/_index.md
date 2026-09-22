---
title: "Aspose::Words::StyleCollection::idx_get method"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::StyleCollection::idx_get method. C++'ta yerel bağımsız tanımlayıcısı ile yerleşik bir stili alır."
type: docs
weight: 11000
url: /tr/cpp/aspose.words/stylecollection/idx_get/
---
## StyleCollection::idx_get(Aspose::Words::StyleIdentifier) method


Yerel bağımsız tanımlayıcısına göre yerleşik bir stili alır.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(Aspose::Words::StyleIdentifier sti)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sti | Aspose::Words::StyleIdentifier | Alınacak yerleşik stili belirten bir [StyleIdentifier](../../styleidentifier/) değeri. |
## Açıklamalar


Henüz mevcut olmayan bir stile erişildiğinde, otomatik olarak oluşturur.

## Örnekler



Bir belgenin stil koleksiyonuna bir [Style](../../style/) nasıl eklenir gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Bu koleksiyona daha sonra ekleyebileceğimiz yeni stiller için varsayılan parametreleri ayarlayın.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Eğer "StyleType.Paragraph" stilini eklersek, koleksiyon değerlerini uygular
// "DefaultParagraphFormat" özelliğini stilin "ParagraphFormat" özelliğine.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Bir stil ekleyin ve ardından varsayılan ayarları içerdiğini doğrulayın.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Ayrıca Bakınız

* Class [Style](../../style/)
* Enum [StyleIdentifier](../../styleidentifier/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(const System::String\&) method


Bir stili adına ya da takma adına göre alır.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(const System::String &name)
```

## Açıklamalar


Büyük/küçük harfe duyarlıdır, verilen isimde stil bulunamazsa **null** döndürür.

Eğer bu, henüz mevcut olmayan yerleşik bir stilin İngilizce adıysa, otomatik olarak oluşturur.

## Örnekler



Belge sayfa düzeninin ne zaman yeniden hesaplanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Bir belgeyi PDF'ye, bir görüntüye kaydetmek ya da ilk kez yazdırmak otomatik olarak
// belgenin sayfaları içinde düzeni önbelleğe alır.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Belgeyi bir şekilde değiştirin.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// Mevcut Aspose.Words sürümünde, belgeyi değiştirmek otomatik olarak yeniden oluşturmaz
// önbelleğe alınmış sayfa düzeni. Önbelleğe alınmış düzeni istersek
// güncel kalması için, manuel olarak güncellememiz gerekecek.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## Ayrıca Bakınız

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(int32_t) method


Bir stili indeksine göre alır.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(int32_t index)
```


## Örnekler



Bir belgenin stil koleksiyonuna bir [Style](../../style/) nasıl eklenir gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Bu koleksiyona daha sonra ekleyebileceğimiz yeni stiller için varsayılan parametreleri ayarlayın.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Eğer "StyleType.Paragraph" stilini eklersek, koleksiyon değerlerini uygular
// "DefaultParagraphFormat" özelliğini stilin "ParagraphFormat" özelliğine.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Bir stil ekleyin ve ardından varsayılan ayarları içerdiğini doğrulayın.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Ayrıca Bakınız

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
