---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign metodu"
linktitle: "get_ReplaceBackslashWithYenSign"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign metodu. Geri eğik çizgi karakterlerinin yen işaretiyle değiştirilip değiştirilmediğini belirtir. Varsayılan değer C++'ta false'tur."
type: docs
weight: 5500
url: /tr/cpp/aspose.words.saving/xamlflowsaveoptions/get_replacebackslashwithyensign/
---
## XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign method


Ters eğik çizgi karakterlerinin yen işaretiyle değiştirilip değiştirilmeyeceğini belirtir. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## Örnekler



Geri eğik çizgi karakterlerinin yen işaretleriyle nasıl değiştirileceğini gösterir (Xaml).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// Varsayılan olarak, Aspose.Words, MS Word davranışını taklit eder ve ters eğik çizgi karakterlerini yen işaretleriyle değiştirmez.
// oluşturulan HTML belgeleri. Ancak, Aspose.Words'un önceki sürümleri belirli
// senaryolarda. Bu bayrak, Aspose.Words'un önceki sürümleriyle geriye dönük uyumluluğu etkinleştirir.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XamlFlowSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

## Ayrıca Bakınız

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
