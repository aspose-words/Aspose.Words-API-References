---
title: "Aspose::Words::HtmlInsertOptions enum"
linktitle: "HtmlInsertOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::HtmlInsertOptions enum. InsertHtml() yönteminin C++'deki seçeneklerini belirtir."
type: docs
weight: 92000
url: /tr/cpp/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enum


[InsertHtml()](../) yöntemi için seçenekleri belirtir.

```cpp
enum class HtmlInsertOptions
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | HTML eklerken varsayılan seçenekleri kullanın. |
| UseBuilderFormatting | 1 | HTML'den eklenen metin için temel biçimlendirme olarak [DocumentBuilder](../documentbuilder/) içinde belirtilen yazı tipi ve paragraf biçimlendirmesini kullanın. |
| RemoveLastEmptyParagraph | 2 | Blok düzeyinde bir öğe ile biten HTML'den sonra normalde eklenen boş paragrafı kaldırın. |
| PreserveBlocks | 4 | Blok düzeyindeki öğelerin özelliklerini koruyun. |


## Örnekler



Görülen kenarlıkların ve kenar boşluklarının daha iyi korunmasını nasıl sağlanacağını gösterir.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                    </div>\r\n                </html>";

// HTML blok düzeyindeki öğelerin içe aktarımının yeni modunu ayarlayın.
Aspose::Words::HtmlInsertOptions insertOptions = Aspose::Words::HtmlInsertOptions::PreserveBlocks;

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
builder->InsertHtml(html, insertOptions);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.PreserveBlocks.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
