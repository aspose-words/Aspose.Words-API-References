---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel metodu"
linktitle: "get_NavigationMapLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel metodu. EPUB, MOBI veya AZW3 formatlarına dışa aktarırken gezinme haritasına doldurulan başlıkların maksimum seviyesini belirtir. Varsayılan değer C++'da %3'tür."
type: docs
weight: 40500
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_navigationmaplevel/
---
## HtmlSaveOptions::get_NavigationMapLevel method


EPUB, MOBI veya AZW3 formatlarına dışa aktarırken gezinme haritasına doldurulan başlıkların maksimum seviyesini belirtir. Varsayılan değer **%3**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel() const
```

## Açıklamalar


Gezinme haritası, kullanıcı ajanlarının belge yapısı içinde kolay bir gezinme yolu sunmasını sağlar. Genellikle gezinme noktaları belgedeki başlıklara karşılık gelir. Başlıkları **N** seviyesine kadar doldurmak için bu değeri [NavigationMapLevel](./) atayın.

Varsayılan olarak, üç seviye başlık doldurulur: **Heading 1**, **Heading 2** ve **Heading 3** stillerine sahip paragraflar. Bu özelliği 1 ile 9 arasında bir değere ayarlayarak ilgili maksimum seviyeyi talep edebilirsiniz. Sıfıra ayarlamak, gezinme haritasını yalnızca belge köküne veya belge bölümlerinin köklerine indirir.

## Örnekler



Azw3 belgeleri için içindekiler tablosu oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Azw3);
options->set_NavigationMapLevel(2);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```


Mobi belgeleri için içindekiler tablosu oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mobi);
options->set_NavigationMapLevel(5);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateMobiToc.mobi", options);
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
