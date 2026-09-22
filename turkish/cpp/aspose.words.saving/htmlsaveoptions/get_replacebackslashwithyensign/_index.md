---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign metodu"
linktitle: "get_ReplaceBackslashWithYenSign"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign metodu. Ters eğik çizgi karakterlerinin yen işaretleriyle değiştirilip değiştirilmeyeceğini belirtir. Varsayılan değer C++'da false'tur."
type: docs
weight: 41500
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_replacebackslashwithyensign/
---
## HtmlSaveOptions::get_ReplaceBackslashWithYenSign method


Ters eğik çizgi karakterlerinin yen işaretiyle değiştirilip değiştirilmeyeceğini belirtir. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## Örnekler



Ters eğik çizgi karakterlerini yen işaretleriyle (Html) nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// Varsayılan olarak, Aspose.Words, MS Word davranışını taklit eder ve ters eğik çizgi karakterlerini yen işaretleriyle değiştirmez.
// oluşturulan HTML belgeleri. Ancak, Aspose.Words'un önceki sürümleri belirli
// senaryolarda. Bu bayrak, Aspose.Words'un önceki sürümleriyle geriye dönük uyumluluğu etkinleştirir.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
