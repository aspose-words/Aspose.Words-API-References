---
title: "Aspose::Words::Loading::BlockImportMode enum"
linktitle: "BlockImportMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::BlockImportMode enum. Gibt an, wie Eigenschaften von Blockelementen aus HTML-basierten Dokumenten in C++ importiert werden."
type: docs
weight: 12000
url: /de/cpp/aspose.words.loading/blockimportmode/
---
## BlockImportMode enum


Gibt an, wie Eigenschaften von Block-Elementen aus HTML-basierten Dokumenten importiert werden.

```cpp
enum class BlockImportMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Merge | 0 | [Properties](../../aspose.words.properties/) der übergeordneten Blöcke werden zusammengeführt und auf Kind-Elementen (z. B. Absätzen oder Tabellen) gespeichert. |
| Preserve | 1 | [Properties](../../aspose.words.properties/) der übergeordneten Blöcke werden in eine spezielle logische Struktur importiert und getrennt von Dokumentknoten gespeichert. |


## Beispiele



Zeigt, wie Eigenschaften von Blockelementen aus HTML-basierten Dokumenten importiert werden.
```cpp
const System::String html = u"\r\n            <html>\r\n                <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                </div>\r\n            </html>";
auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html));

auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
// Setzt den neuen Modus für den Import von HTML-Blockelementen.
loadOptions->set_BlockImportMode(blockImportMode);

auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BlockImport.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
