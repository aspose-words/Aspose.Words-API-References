---
title: "Aspose::Words::Document::UpdateFields metodu"
linktitle: "UpdateFields"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::UpdateFields metodu. C++'ta tüm belgede alanların değerlerini günceller."
type: docs
weight: 96000
url: /tr/cpp/aspose.words/document/updatefields/
---
## Document::UpdateFields method


Tüm belgede alan değerlerini günceller.

```cpp
void Aspose::Words::Document::UpdateFields()
```

## Açıklamalar


Bir belgeyi açıp, değiştirip ardından kaydettiğinizde, Aspose.Words alanları otomatik olarak güncellemez, onları aynı tutar. Bu nedenle, belgeyi programlı olarak değiştirdiyseniz ve kaydedilen belgede doğru (hesaplanmış) alan değerlerinin görünmesini sağlamak istiyorsanız, genellikle kaydetmeden önce bu metodu çağırmak istersiniz.

Posta birleştirme işlemi gerçekleştirdikten sonra alanları güncellemenize gerek yoktur, çünkü posta birleştirme bir alan güncellemesi türüdür ve belgedeki tüm alanları otomatik olarak günceller.

Bu metod tüm alan türlerini güncellemez. Desteklenen alan türlerinin ayrıntılı listesi için Programcılar Kılavuzuna bakın.

Bu metod, sayfa düzeni algoritmalarıyla ilgili alanları (ör. PAGE, PAGES, PAGEREF) güncellemez. Sayfa düzeniyle ilgili alanlar, bir belgeyi renderladığınızda veya [UpdatePageLayout](../updatepagelayout/) metodunu çağırdığınızda güncellenir.

Alan türlerini etkileyen belge değişiklikleri olduysa, alanları güncellemeden önce [NormalizeFieldTypes](../normalizefieldtypes/) metodunu kullanın.

Belgenin belirli bir bölümündeki alanları güncellemek için [UpdateFields](../../range/updatefields/) metodunu kullanın.

## Örnekler



Başlık stillerini giriş olarak kullanarak bir belgeye İçindekiler Tablosu (TOC) eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgenin ilk sayfası için bir içindekiler tablosu ekleyin.
// Tabloyu, 1 ila 3 seviyelerindeki başlıklarla paragraf alacak şekilde yapılandırın.
// Ayrıca, girdilerini bizi yönlendirecek hiperlinkler olarak ayarlayın
// Microsoft Word'de sol tıklandığında başlığın konumuna.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// İçindekiler tablosunu, başlık stilleriyle paragraflar ekleyerek doldurun.
// 1 ile 3 arasında bir seviyeye sahip her başlık, tabloda bir giriş oluşturur.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// İçindekiler tablosu, güncel bir sonuç göstermek için güncellenmesi gereken bir tür alanıdır.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


QUOTE alanının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir QUOTE alanı ekleyin; bu, Text özelliğinin değerini görüntüler.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Bir QUOTE alanı ekleyin ve içine bir DATE alanı yerleştirin.
// DATE alanları, belgeyi Microsoft Word ile her açtığımızda değerlerini geçerli tarihe günceller.
// DATE alanını QUOTE alanının içine bu şekilde yerleştirmek, değerini dondurur
// belgeyi oluşturduğumuz tarihe.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Tüm alanları doğru sonuçlarını gösterecek şekilde güncelleyin.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```


Kullanıcı ayrıntılarını nasıl ayarlayacağınızı ve alanları kullanarak nasıl görüntüleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir UserInformation nesnesi oluşturun ve bunu kullanıcı bilgilerini görüntüleyen alanlar için veri kaynağı olarak ayarlayın.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// USERNAME, USERINITIALS ve USERADDRESS alanlarını ekleyin; bu alanlar değerlerini gösterir
// yukarıda oluşturduğumuz UserInformation nesnesinin ilgili özelliklerini.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// Alan seçenekleri nesnesi ayrıca tüm belgelerden alanların başvurabileceği statik bir varsayılan kullanıcı içerir.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
