---
title: "Aspose::Words::Document::JoinRunsWithSameFormatting method"
linktitle: "JoinRunsWithSameFormatting"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::JoinRunsWithSameFormatting yöntemi. C++'ta belgenin tüm paragraflarında aynı biçimlendirmeye sahip run'ları birleştirir."
type: docs
weight: 65000
url: /tr/cpp/aspose.words/document/joinrunswithsameformatting/
---
## Document::JoinRunsWithSameFormatting method


Belgedeki tüm paragraflarda aynı biçimlendirmeye sahip koşulları birleştirir.

```cpp
int32_t Aspose::Words::Document::JoinRunsWithSameFormatting()
```


### ReturnValue

Gerçekleştirilen birleştirme sayısı. **N** ardışık run birleştirildiğinde, **N - 1** birleştirme olarak sayılır.
## Açıklamalar


Bu bir optimizasyon yöntemidir. Bazı belgeler aynı biçimlendirmeye sahip ardışık run'lar içerir. Genellikle bu, bir belgenin yoğun bir şekilde manuel olarak düzenlenmesi durumunda ortaya çıkar. Bu run'ları birleştirerek belge boyutunu azaltabilir ve sonraki işlemleri hızlandırabilirsiniz.

İşlem, belgede bulunan her [Paragraph](../../paragraph/) düğümünü, aynı özelliklere sahip ardışık [Run](../../run/) düğümleri için kontrol eder. Run oluşturma ve değiştirme oturumlarını izlemek için kullanılan benzersiz tanımlayıcıları yok sayar. Her bir birleştirme dizisindeki ilk run tüm metni biriktirir. Kalan run'lar belgeden silinir.

## Örnekler



Gereksiz run'ları azaltmak için bir belgede run'ların nasıl birleştirileceğini gösterir.
```cpp
// Aynı biçimlendirmeye sahip ardışık metin run'ları içeren bir belge açın,
// bu, aynı paragrafı Microsoft Word'de birden çok kez düzenlediğimizde yaygın olarak ortaya çıkar.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Bu run'ların herhangi bir sayısı aynı biçimlendirmeye sahip ardışık ise,
// belge sadeleştirilebilir.
ASSERT_EQ(317, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());

// Bu yöntemi kullanarak bu run'ları birleştirin ve gerçekleşecek run birleştirme sayısını doğrulayın.
ASSERT_EQ(121, doc->JoinRunsWithSameFormatting());

// Birleştirme sonrası sahip olduğumuz birleştirme sayısı ve run sayısı
// başlangıçta sahip olduğumuz run sayısına eşit olmalıdır.
ASSERT_EQ(196, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
