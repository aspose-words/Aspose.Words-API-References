---
title: "Aspose::Words::DocumentBuilder::InsertHyperlink metodu"
linktitle: "InsertHyperlink"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertHyperlink metodu. C++'ta belgeye bir köprü ekler."
type: docs
weight: 38000
url: /tr/cpp/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder::InsertHyperlink method


Belgeye bir köprü ekler.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertHyperlink(const System::String &displayText, const System::String &urlOrBookmark, bool isBookmark)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| displayText | const System::String\& | Belgede görüntülenecek bağlantının metni. |
| urlOrBookmark | const System::String\& | Bağlantı hedefi. Bir URL veya belgedeki bir yer imi adı olabilir. Bu metod, URL'nin başına ve sonuna her zaman tek tırnak ekler. |
| isBookmark | bool | **true** eğer önceki parametre belgedeki bir yer imi adı ise; **false** eğer önceki parametre bir URL ise. |

### ReturnValue

Eklenen alanı temsil eden bir [Field](../../../aspose.words.fields/field/) nesnesi.
## Açıklamalar


Köprü görüntü metni için yazı tipi biçimlendirmesini açıkça [Font](../get_font/) özelliğini kullanarak belirtmeniz gerektiğini unutmayın.

Bu metod, belgeye bir MS Word HYPERLINK alanı eklemek için dahili olarak [InsertField()](../) metodunu çağırır.

## Örnekler



Bir hiperlink alanının nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Bir hiperlink ekleyin ve özel biçimlendirme ile vurgulayın.
// Hiperlink, URL'de belirtilen konuma götürecek tıklanabilir bir metin parçası olacaktır.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Microsoft Word'de metindeki bağlantıya Ctrl + sol tıklama, yeni bir web tarayıcı penceresi aracılığıyla URL'ye götürür.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


Bir belge oluşturucusunun biçimlendirme yığını nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yazı tipi biçimlendirmesini ayarlayın, ardından köprüden önce gelen metni yazın.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Mevcut biçimlendirme yapılandırmamızı yığında koruyun.
builder->PushFont();

// Yeni bir stil uygulayarak oluşturucunun mevcut biçimlendirmesini değiştirin.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Daha önce kaydettiğimiz yazı tipi biçimlendirmesini geri yükleyin ve öğeyi yığından kaldırın.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```


Yerel bir yer imi referans veren bir köprünün nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// Yer imiyle bağlantı kuran bir HYPERLINK alanı ekleyin. Alan anahtarlarını
// "InsertHyperlink" metoduna, referans verilen yer iminin adını içeren argümanın bir parçası olarak geçirebiliriz.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## Ayrıca Bakınız

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
