---
title: "Aspose::Words::Loading::BlockImportMode enum"
linktitle: "BlockImportMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::BlockImportMode enum. HTML tabanlı belgelerden blok düzeyindeki öğelerin özelliklerinin C++'ta nasıl içe aktarıldığını belirtir."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.loading/blockimportmode/
---
## BlockImportMode enum


Blok düzeyindeki öğelerin özelliklerinin HTML tabanlı belgelere nasıl aktarıldığını belirtir.

```cpp
enum class BlockImportMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Merge | 0 | [Properties](../../aspose.words.properties/) ebeveyn blokların özellikleri birleştirilir ve alt öğelere (yani paragraflara veya tablolara) depolanır. |
| Preserve | 1 | [Properties](../../aspose.words.properties/) ebeveyn blokların özellikleri özel bir mantıksal yapıya içe aktarılır ve belge düğümlerinden ayrı olarak depolanır. |


## Örnekler



Blok düzeyindeki öğelerin özelliklerinin HTML tabanlı belgelerden nasıl içe aktarıldığını gösterir.
```cpp
const System::String html = u"\r\n            <html>\r\n                <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                </div>\r\n            </html>";
auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html));

auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
// HTML blok düzeyindeki öğelerin içe aktarımının yeni modunu ayarlayın.
loadOptions->set_BlockImportMode(blockImportMode);

auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BlockImport.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
