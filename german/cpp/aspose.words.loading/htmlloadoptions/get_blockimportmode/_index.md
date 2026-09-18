---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode Methode"
linktitle: "get_BlockImportMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode Methode. Gibt einen Wert zurück oder legt ihn fest, der angibt, wie Eigenschaften von Block‑Elementen importiert werden. Der Standardwert ist Merge in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.loading/htmlloadoptions/get_blockimportmode/
---
## HtmlLoadOptions::get_BlockImportMode method


Gibt einen Wert zurück oder legt ihn fest, der angibt, wie Eigenschaften von Block‑Elementen importiert werden. Der Standardwert ist [Merge](../../blockimportmode/).

```cpp
Aspose::Words::Loading::BlockImportMode Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode() const
```


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

* Enum [BlockImportMode](../../blockimportmode/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
