---
title: "Aspose::Words::NumSpacing enum"
linktitle: "NumSpacing"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NumSpacing enum. C++'da sayı aralığının görüntülenebileceği olası değerleri belirtir."
type: docs
weight: 103500
url: /tr/cpp/aspose.words/numspacing/
---
## NumSpacing enum


Sayısal boşlukların gösterilebileceği olası değerleri belirtir.

```cpp
enum class NumSpacing
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Default | 0 | Sayıların yazı tipinin varsayılan biçiminde görüntülendiğini belirtir. |
| Orantılı | 1 | Yazı tipi destekliyorsa, orantılı aralıklı olarak tasarlanmış sayı biçimlerinin görüntülendiğini belirtir. |
| Tablo | 2 | Yazı tipi destekliyorsa, tablo şeklinde tasarlanmış sayı biçimlerinin görüntülenmesini belirtir. |


## Örnekler



Sayının boşluk tipinin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bu etki yalnızca MS Word'ün daha yeni sürümlerinde desteklenir.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
