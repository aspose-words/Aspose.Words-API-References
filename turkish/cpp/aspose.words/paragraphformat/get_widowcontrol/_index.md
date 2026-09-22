---
title: "Aspose::Words::ParagraphFormat::get_WidowControl yöntemi"
linktitle: "get_WidowControl"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_WidowControl yöntemi. Paragraftaki ilk ve son satırların, paragrafın geri kalanıyla aynı sayfada kalması gerekiyorsa true döner."
type: docs
weight: 41000
url: /tr/cpp/aspose.words/paragraphformat/get_widowcontrol/
---
## ParagraphFormat::get_WidowControl method


Paragraftaki ilk ve son satırların, paragrafın geri kalanıyla aynı sayfada kalması gerekiyorsa doğru.

```cpp
bool Aspose::Words::ParagraphFormat::get_WidowControl()
```


## Örnekler



Bir paragrafta widow/orphan kontrolünü nasıl etkinleştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir sayfaya sığmayan metni yazdığımızda, bir satır bir sonraki sayfaya taşabilir.
// Bir sonraki sayfada kalan tek satıra "Orphan" denir,
// ve yetimin kırıldığı önceki satıra "Widow" denir.
// Yazı tipini, boşlukları veya sayfa kenar boşluklarını değiştirerek yetimler ve dul satırları düzeltebiliriz.
// Belgenin boyutlarını korumak istiyorsak, bu bayrağı "true" olarak ayarlayabiliriz
// dul satırları ilgili yetim satırlarıyla aynı sayfaya itmek için.
// Bu bayrağı "false" olarak bırakmak, metinde widow/orphan çiftlerinin kalmasına neden olur.
// Her paragrafta bu ayar, Microsoft Word'de Ana Sayfa -> Paragraf -> Paragraf Ayarları üzerinden erişilebilir.
// ("Paragraf" sekmesinin sağ alt köşesindeki düğme) -> "Widow/Orphan control".
builder->get_ParagraphFormat()->set_WidowControl(widowControl);

// Bir yetim ve bir dul oluşturan metin ekleyin.
builder->get_Font()->set_Size(68);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.WidowControl.docx");
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
