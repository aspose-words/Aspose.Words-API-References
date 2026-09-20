---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode метод"
linktitle: "get_BlockImportMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode метод. Получает или задает значение, определяющее, как импортируются свойства блочных элементов. Значение по умолчанию — Merge в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.loading/htmlloadoptions/get_blockimportmode/
---
## HtmlLoadOptions::get_BlockImportMode method


Получает или задает значение, определяющее, как импортируются свойства блочных элементов. Значение по умолчанию — [Merge](../../blockimportmode/).

```cpp
Aspose::Words::Loading::BlockImportMode Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode() const
```


## Примеры



Показывает, как свойства блочных элементов импортируются из HTML‑документов.
```cpp
const System::String html = u"\r\n            <html>\r\n                <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                </div>\r\n            </html>";
auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html));

auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
// Установите новый режим импорта блочных элементов HTML.
loadOptions->set_BlockImportMode(blockImportMode);

auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BlockImport.docx");
```

## См. также

* Enum [BlockImportMode](../../blockimportmode/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
