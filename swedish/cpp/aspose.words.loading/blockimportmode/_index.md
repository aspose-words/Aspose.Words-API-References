---
title: "Aspose::Words::Loading::BlockImportMode enum"
linktitle: "BlockImportMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::BlockImportMode enum. Anger hur egenskaper för blocknivåelement importeras från HTML‑baserade dokument i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.loading/blockimportmode/
---
## BlockImportMode enum


Anger hur egenskaper för blocknivåelement importeras från HTML‑baserade dokument.

```cpp
enum class BlockImportMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Merge | 0 | [Properties](../../aspose.words.properties/) för föräldra‑block slås samman och lagras på underordnade element (dvs. stycken eller tabeller). |
| Preserve | 1 | [Properties](../../aspose.words.properties/) för föräldra‑block importeras till en speciell logisk struktur och lagras separat från dokumentnoder. |


## Exempel



Visar hur egenskaper för blocknivåelement importeras från HTML‑baserade dokument.
```cpp
const System::String html = u"\r\n            <html>\r\n                <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                </div>\r\n            </html>";
auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html));

auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
// Ställ in det nya läget för import av HTML‑blocknivåelement.
loadOptions->set_BlockImportMode(blockImportMode);

auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BlockImport.docx");
```

## Se även

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
