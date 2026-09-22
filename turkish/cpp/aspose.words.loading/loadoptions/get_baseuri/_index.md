---
title: "Aspose::Words::Loading::LoadOptions::get_BaseUri yöntemi"
linktitle: "get_BaseUri"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_BaseUri yöntemi. Belgede bulunan göreli URI'leri gerektiğinde mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır veya ayarlar. Null veya boş dize olabilir. Varsayılan değer C++'da null'dur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.loading/loadoptions/get_baseuri/
---
## LoadOptions::get_BaseUri method


Belgede bulunan göreceli URI'leri gerektiğinde mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır veya ayarlar. **null** veya boş dize olabilir. Varsayılan **null**'dır.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_BaseUri() const
```

## Açıklamalar


Bu özellik aşağıdaki durumlarda göreli URI'leri mutlak URI'lere dönüştürmek için kullanılır:

1. Bir akıştan HTML belgesi yüklenirken ve belge göreli URI'lere sahip görüntüler içerdiğinde ve BASE HTML öğesinde bir temel URI belirtilmemişse.
1. Bir belge PDF ve diğer formatlara kaydedilirken, göreli URI'lerle bağlanmış görüntüleri almak için, böylece görüntüler çıktı belgesine kaydedilebilir.



## Örnekler



Bir akıştan temel URI kullanarak görüntülü bir HTML belgesinin nasıl açılacağını gösterir.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // Yüklerken temel klasörün URI'sını geçirin
    // böylece HTML belgesindeki göreli URI'li tüm görüntüler bulunabilir.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // Belgenin ilk şeklinin geçerli bir görüntü içerdiğini doğrulayın.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## Ayrıca Bakınız

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
