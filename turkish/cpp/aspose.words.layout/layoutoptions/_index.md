---
title: "Aspose::Words::Layout::LayoutOptions sınıfı"
linktitle: "LayoutOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutOptions sınıfı. Belge yerleşim sürecini kontrol etmeyi sağlayan seçenekleri tutar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.layout/layoutoptions/
---
## LayoutOptions class


Belge düzeni sürecini kontrol etmeyi sağlayan seçenekleri tutar. Daha fazla bilgi için, [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) dokümantasyon makalesini ziyaret edin.

```cpp
class LayoutOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Callback](./get_callback/)() const | Sayfa yerleşim modeli tarafından kullanılan [IPageLayoutCallback](../ipagelayoutcallback/) uygulamasını alır. |
| [get_CommentDisplayMode](./get_commentdisplaymode/)() const | Yorumların nasıl görüntüleneceğini alır veya ayarlar. Varsayılan değer [ShowInBalloons](../commentdisplaymode/). |
| [get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/)() const | Sürekli bir bölüm sayfa numaralandırmasını yeniden başlattığında sayfa numaralarını hesaplama davranış modunu alır veya ayarlar. |
| [get_IgnorePrinterMetrics](./get_ignoreprintermetrics/)() const | \"Belgeyi yerleştirmek için yazıcı ölçümleri kullan\" uyumluluk seçeneğinin göz ardı edilip edilmediğini gösteren değeri alır veya ayarlar. Varsayılan **true**. |
| [get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/)() const | Yazı tipi ikamesinden sonra orijinal yazı tipi ölçümlerinin kullanılıp kullanılmayacağını gösteren değeri alır veya ayarlar. Varsayılan **true**. |
| [get_RevisionOptions](./get_revisionoptions/)() const | Revizyon seçeneklerini alır. |
| [get_ShowHiddenText](./get_showhiddentext/)() const | Belgedeki gizli metnin görüntülenip görüntülenmeyeceğini gösteren değeri alır veya ayarlar. Varsayılan **false**. |
| [get_ShowParagraphMarks](./get_showparagraphmarks/)() const | Paragraf işaretlerinin görüntülenip görüntülenmeyeceğini gösteren değeri alır veya ayarlar. Varsayılan **false**. |
| [get_TextShaperFactory](./get_textshaperfactory/)() const | Gelişmiş Tipografi render özellikleri için kullanılan [ITextShaperFactory](../) uygulamasını alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutOptions](./layoutoptions/)() |  |
| [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::Layout::IPageLayoutCallback\>\&) | Sayfa yerleşim modeli tarafından kullanılan [IPageLayoutCallback](../ipagelayoutcallback/) uygulamasını ayarlar. |
| [set_CommentDisplayMode](./set_commentdisplaymode/)(Aspose::Words::Layout::CommentDisplayMode) | Ayarlayıcı [Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode](./get_commentdisplaymode/). |
| [set_ContinuousSectionPageNumberingRestart](./set_continuoussectionpagenumberingrestart/)(Aspose::Words::Layout::ContinuousSectionRestart) | Ayarlayıcı [Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/). |
| [set_IgnorePrinterMetrics](./set_ignoreprintermetrics/)(bool) | Ayarlayıcı [Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics](./get_ignoreprintermetrics/). |
| [set_KeepOriginalFontMetrics](./set_keeporiginalfontmetrics/)(bool) | Ayarlayıcı [Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/). |
| [set_ShowHiddenText](./set_showhiddentext/)(bool) | Ayarlayıcı [Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText](./get_showhiddentext/). |
| [set_ShowParagraphMarks](./set_showparagraphmarks/)(bool) | Ayarlayıcı [Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks](./get_showparagraphmarks/). |
| [set_TextShaperFactory](./set_textshaperfactory/)(const System::SharedPtr\<Aspose::Words::Shaping::ITextShaperFactory\>\&) | Gelişmiş Tipografi render özellikleri için kullanılan [ITextShaperFactory](../) uygulamasını ayarlar. |
| static [Type](./type/)() |  |
## Açıklamalar


Bu sınıfın örneklerini doğrudan oluşturamazsınız. Bu belge için yerleşim seçeneklerine erişmek üzere [LayoutOptions](../../aspose.words/document/get_layoutoptions/) özelliğini kullanın.

Bu sınıfta bulunan seçeneklerden herhangi birini değiştirdikten sonra, değiştirilen seçeneklerin yerleşime uygulanması için [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) yönteminin çağrılması gerektiğini unutmayın.

## Örnekler



Bir oluşturulmuş çıktı belgesinde metnin nasıl gizleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Gizli metni ekleyin, ardından bunu oluşturulmuş bir belgeden çıkarıp çıkarmak istemediğinizi belirtin.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


Bir oluşturulmuş çıktı belgesinde paragraf işaretlerinin nasıl gösterileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bazı paragraflar ekleyin, ardından paragraf işaretlerini etkinleştirerek paragrafların sonlarını gösterin
// belgeyi oluşturduğumuzda pilcrow (¶) sembolüyle.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


Bir oluşturulmuş çıktı belgesinde revizyonların görünümünün nasıl değiştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir revizyon ekleyin, ardından tüm revizyonların rengini yeşile değiştirin.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Her revize edilmiş satırın solunda görünen çubuğu kaldırın.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
