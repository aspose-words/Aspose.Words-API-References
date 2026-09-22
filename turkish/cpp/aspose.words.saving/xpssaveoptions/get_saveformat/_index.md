---
title: "Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat yöntemi"
linktitle: "get_SaveFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat yöntemi. Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği biçimi belirtir. C++'ta yalnızca Xps olabilir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/xpssaveoptions/get_saveformat/
---
## XpsSaveOptions::get_SaveFormat method


Bu kaydetme seçenekleri nesnesi kullanıldığında belgenin kaydedileceği biçimi belirtir. Yalnızca [Xps](../../../aspose.words/saveformat/) olabilir.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::XpsSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
