---
title: "Aspose::Words::JoinRunsOptions sınıfı"
linktitle: "JoinRunsOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::JoinRunsOptions sınıfı. C++'ta birleştirme işlemi için yapılandırma bayrakları sağlar."
type: docs
weight: 38500
url: /tr/cpp/aspose.words/joinrunsoptions/
---
## JoinRunsOptions class


Birleştirme çalıştırma işlemi için yapılandırma bayrakları sağlar.

```cpp
class JoinRunsOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_IgnoreInsignificant](./get_ignoreinsignificant/)() const | True, aynı biçimlendirmeye sahip çalıştırmaları birleştirirken tüm çalıştırmaların önemsiz özniteliklerinin yok sayılacağını gösterir. |
| [get_IgnoreRedundant](./get_ignoreredundant/)() const | True, aynı biçimlendirmeye sahip çalıştırmaları birleştirirken tüm çalıştırmaların gereksiz özniteliklerinin yok sayılacağını gösterir. |
| [get_IgnoreSpacing](./get_ignorespacing/)() const | True, aynı biçimlendirmeye sahip çalıştırmaları birleştirirken tüm çalıştırmaların boşluk özniteliklerinin yok sayılacağını gösterir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [JoinRunsOptions](./joinrunsoptions/)() |  |
| [set_IgnoreInsignificant](./set_ignoreinsignificant/)(bool) | True, aynı biçimlendirmeye sahip çalıştırmaları birleştirirken tüm çalıştırmaların önemsiz özniteliklerinin yok sayılacağını gösterir. |
| [set_IgnoreRedundant](./set_ignoreredundant/)(bool) | True, aynı biçimlendirmeye sahip çalıştırmaları birleştirirken tüm çalıştırmaların gereksiz özniteliklerinin yok sayılacağını gösterir. |
| [set_IgnoreSpacing](./set_ignorespacing/)(bool) | True, aynı biçimlendirmeye sahip çalıştırmaları birleştirirken tüm çalıştırmaların boşluk özniteliklerinin yok sayılacağını gösterir. |
| static [Type](./type/)() |  |

## Örnekler



Aynı biçimlendirmeye sahip çalıştırmaları, gereksiz ve önemsiz öznitelikleri yok sayarak nasıl birleştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Görünür biçimlendirmesi aynı ancak bazı içsel farklılıkları olan çalıştırmalar oluşturun.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// Birleştirmeden önce çalıştırmaları doğrulayın.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// Birleştirme sırasında gereksiz ve önemsiz öznitelikleri yok saymak için seçenekleri yapılandırın.
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// Görünümü etkilemeyen gereksiz çalıştırma özelliklerini yok sayın.
options->set_IgnoreInsignificant(true);
// Yalnızca boşluk içeren çalıştırmalar gibi önemsiz farkları yok sayın.

// Genişletilmiş seçenekleri kullanarak aynı görünür biçimlendirmeye sahip run'ları birleştirin.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// Run'ların başarıyla birleştirildiğini doğrulayın.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
