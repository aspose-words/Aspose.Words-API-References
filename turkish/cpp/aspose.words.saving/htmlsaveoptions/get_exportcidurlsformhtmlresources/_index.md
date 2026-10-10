---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources metodu"
linktitle: "get_ExportCidUrlsForMhtmlResources"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources metodu. MHTML belgelerinde yer alan kaynaklara (görseller, yazı tipleri, CSS) referans vermek için CID (Content-ID) URL'lerinin kullanılıp kullanılmayacağını belirtir. Varsayılan değer C++'da false'tur."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exportcidurlsformhtmlresources/
---
## HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method


MHTML belgelerinde bulunan kaynakları (görseller, yazı tipleri, CSS) referanslamak için CID (Content-ID) URL'lerinin kullanılıp kullanılmayacağını belirtir. Varsayılan değer **false**'tur.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources() const
```

## Açıklamalar


Bu seçenek yalnızca MHTML olarak kaydedilen belgeleri etkiler.

Varsayılan olarak, MHTML belgelerindeki kaynaklar dosya adıyla (örneğin, "image.png") referans gösterilir ve bu adlar MIME parçalarının "Content-Location" başlıklarıyla eşleştirilir.

Bu seçenek, kaynak dosyalarına referansların CID (Content-ID) URL'leri (örneğin, "cid:image.png") olarak yazıldığı alternatif bir yöntemi etkinleştirir ve bu referanslar "Content-ID" başlıklarıyla eşleştirilir.

Teoride, iki referans yönteminin arasında bir fark olmamalı ve her ikisi de herhangi bir tarayıcı ya da e-posta istemcisinde sorunsuz çalışmalıdır. Ancak pratikte, bazı istemciler dosya adıyla kaynakları almayı başaramaz. Tarayıcınız veya e-posta istemciniz bir MTHML belgesindeki (görselleri göstermez veya CSS stillerini yüklemez) kaynakları yüklemeyi reddederse, belgeyi CID URL'leriyle dışa aktarmayı deneyin.

## Örnekler



Çıktı MHTML belgeleri için içerik kimliklerinin nasıl etkinleştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Bu bayrağı ayarlamak "Content-Location" etiketlerini değiştirecek
// giriş belgesindeki her kaynak için "Content-ID" etiketleriyle.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mhtml);
options->set_ExportCidUrlsForMhtmlResources(exportCidUrlsForMhtmlResources);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-ID: <document.html>"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-Location: document.html"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
