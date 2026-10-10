---
title: "Aspose::Words::Fonts::EmbeddedFontFormat enum"
linktitle: "EmbeddedFontFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::EmbeddedFontFormat enum. Belirli bir gömülü fontun FontInfo nesnesi içindeki biçimini belirtir. Bir belgeyi dosyaya kaydederken, yalnızca ilgili biçimdeki gömülü fontlar C++'ta yazılır."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enum


Belirli bir gömülü fontun [FontInfo](../fontinfo/) nesnesi içindeki biçimini belirtir. Bir belgeyi dosyaya kaydederken, yalnızca ilgili biçimdeki gömülü fontlar yazılır.

```cpp
enum class EmbeddedFontFormat
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| EmbeddedOpenType | 0 | Gömülü OpenType (EOT) Dosya Biçimini belirtir. Bu gömülü font biçimi DOC dosyalarında kullanılır. |
| OpenType | 1 | OpenType (TrueType) font dosyasının sade bir kopyası olarak gömülmüş fontu belirtir. Bu gömülü font biçimi Open Office XML formatında, DOCX dosyaları dahil, kullanılır. |


## Örnekler



Bir belgeden gömülü bir yazı tipinin nasıl çıkarılacağını ve yerel dosya sistemine nasıl kaydedileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfo> embeddedFont = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift");
System::ArrayPtr<uint8_t> embeddedFontBytes = embeddedFont->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Gömülü yazı tipi biçimleri, .doc gibi diğer biçimlerde farklı olabilir.
// Yazı tipini çıkarabilmek için doğru biçimi bilmemiz gerekir.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.doc");

ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::EmbeddedOpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));

// Ayrıca, .doc belgelerinden gelen gömülü OpenType biçimini OpenType’a dönüştürebiliriz.
embeddedFontBytes = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
