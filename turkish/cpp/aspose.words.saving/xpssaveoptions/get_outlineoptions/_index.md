---
title: "Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions metodu"
linktitle: "get_OutlineOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions yöntemi. C++'ta anahat seçeneklerini belirtmeye izin verir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.saving/xpssaveoptions/get_outlineoptions/
---
## XpsSaveOptions::get_OutlineOptions method


Anahat seçeneklerini belirtmeye izin verir.

```cpp
System::SharedPtr<Aspose::Words::Saving::OutlineOptions> Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions() const
```

## Açıklamalar


XPS'ye kaydederken [ExpandedOutlineLevels](../../outlineoptions/get_expandedoutlinelevels/) seçeneğinin çalışmayacağını unutmayın.

## Örnekler



Kaydedilen bir XPS belgesinin taslak (outline) içinde görünecek başlık seviyelerinin nasıl sınırlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Seviye 1, 2 ve ardından 3 olan başlıkları, TOC (İçindekiler) girdileri olarak ekleyin.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// \"XpsSaveOptions\" nesnesi oluşturun; bu nesneyi belgenin \"Save\" yöntemine geçebiliriz
// bu yöntemin belgeyi .XPS'ye nasıl dönüştürdüğünü değiştirmek için.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// Çıktı XPS belgesi bir taslak, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu içerecektir.
// Bu taslaktaki bir girdiye tıklamak, ilgili başlığın konumuna götürür.
// \"HeadingsOutlineLevels\" özelliğini \"2\" olarak ayarlayın; böylece seviyeleri 2'nin üzerindeki tüm başlıklar taslaktan dışlanır.
// Yukarıda eklediğimiz son iki başlık görünmeyecek.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## Ayrıca Bakınız

* Class [OutlineOptions](../../outlineoptions/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
