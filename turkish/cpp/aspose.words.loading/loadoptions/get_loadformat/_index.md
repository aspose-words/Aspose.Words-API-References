---
title: "Aspose::Words::Loading::LoadOptions::get_LoadFormat method"
linktitle: "get_LoadFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_LoadFormat yöntemi. Yüklenecek belgenin formatını belirtir. Varsayılan C++'da Auto'dur."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.loading/loadoptions/get_loadformat/
---
## LoadOptions::get_LoadFormat method


Yüklenecek belgenin formatını belirtir. Varsayılan [Auto](../../../aspose.words/loadformat/)'dır.

```cpp
Aspose::Words::LoadFormat Aspose::Words::Loading::LoadOptions::get_LoadFormat() const
```

## Açıklamalar


Dosya formatını otomatik olarak algılaması için Aspose.Words'ün [Auto](../../../aspose.words/loadformat/) değerini belirtmeniz ve bırakmanız önerilir. Yüklemek üzere olduğunuz belgenin formatını biliyorsanız, formatı açıkça belirtebilir ve bu, formatın otomatik algılanmasıyla ilgili ek yükü azaltarak yükleme süresini biraz kısaltır. Açık bir yükleme formatı belirtir ve bu format yanlış çıkarsa, otomatik algılama devreye girer ve dosyayı ikinci bir kez yüklemeye çalışılır.

## Örnekler



Bir html belgesi açılırken temel URI'nin nasıl belirtileceğini gösterir.
```cpp
// .html belgesi içinde göreli bir URI ile bağlanmış bir resmi yüklemek istediğimizi varsayalım
// Resim farklı bir konumda iken. Bu durumda, göreli URI'yi mutlak bir URI'ye dönüştürmemiz gerekir.
// Bir HtmlLoadOptions nesnesi kullanarak temel URI sağlayabiliriz.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Giriş .html dosyasındaki resim bozuk olsa da, özel temel URI'muz bağlantıyı onarmamıza yardımcı oldu.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Bu çıktı belgesi eksik olan resmi gösterecek.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Ayrıca Bakınız

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
