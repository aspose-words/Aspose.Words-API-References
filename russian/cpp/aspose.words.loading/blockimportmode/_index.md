---
title: "Aspose::Words::Loading::BlockImportMode enum"
linktitle: "BlockImportMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::BlockImportMode enum. Указывает, как свойства блочных элементов импортируются из HTML‑документов в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.loading/blockimportmode/
---
## BlockImportMode enum


Указывает, как свойства блочных элементов импортируются из HTML‑документов.

```cpp
enum class BlockImportMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Merge | 0 | [Свойства](../../aspose.words.properties/) родительских блоков объединяются и сохраняются в дочерних элементах (т. е. абзацах или таблицах). |
| Preserve | 1 | [Свойства](../../aspose.words.properties/) родительских блоков импортируются в специальную логическую структуру и хранятся отдельно от узлов документа. |


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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
