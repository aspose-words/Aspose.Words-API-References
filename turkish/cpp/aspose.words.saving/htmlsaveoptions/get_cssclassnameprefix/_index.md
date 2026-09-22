---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix metodu"
linktitle: "get_CssClassNamePrefix"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix metodu. Tüm CSS sınıf adlarına eklenen bir önek belirtir. Varsayılan değer boş bir dizedir ve oluşturulan CSS sınıf adlarının C++'da ortak bir öneki yoktur."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_cssclassnameprefix/
---
## HtmlSaveOptions::get_CssClassNamePrefix method


Tüm CSS sınıf adlarına eklenen bir önek belirtir. Varsayılan değer boş bir dizedir ve oluşturulan CSS sınıf adlarında ortak bir önek bulunmaz.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix() const
```

## Açıklamalar


Bu değer boş değilse, Aspose.Words tarafından oluşturulan tüm CSS sınıfları belirtilen önek ile başlayacaktır. Bu, örneğin, oluşturulan belgelere özel CSS eklediğinizde ve sınıf adı çakışmalarını önlemek istediğinizde faydalı olabilir.

Değer **null** değilse veya boş değilse, geçerli bir CSS tanımlayıcısı olmalıdır.

## Örnekler



Bir belgeyi HTML olarak kaydetmeyi ve tüm CSS sınıf adlarına bir önek eklemeyi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
saveOptions->set_CssClassNamePrefix(u"myprefix-");

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.html");

ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Header\">"));
ASSERT_TRUE(outDocContents.Contains(u"<p class=\"myprefix-Footer\">"));

outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.CssClassNamePrefix.css");

ASSERT_TRUE(outDocContents.Contains(u".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
ASSERT_TRUE(outDocContents.Contains(u".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
