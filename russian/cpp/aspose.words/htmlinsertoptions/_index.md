---
title: "Перечисление Aspose::Words::HtmlInsertOptions"
linktitle: "HtmlInsertOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::HtmlInsertOptions enum. Указывает параметры для метода InsertHtml() в C++."
type: docs
weight: 92000
url: /ru/cpp/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enum


Указывает параметры для метода [InsertHtml()](../).

```cpp
enum class HtmlInsertOptions
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Используйте параметры по умолчанию при вставке HTML. |
| UseBuilderFormatting | 1 | Используйте шрифтовое и абзацное форматирование, указанное в [DocumentBuilder](../documentbuilder/), в качестве базового форматирования для текста, вставленного из HTML. |
| RemoveLastEmptyParagraph | 2 | Удалить пустой абзац, который обычно вставляется после HTML, заканчивающегося блочным элементом. |
| PreserveBlocks | 4 | Сохранять свойства блочных элементов. |


## Примеры



Показывает, как лучше сохранять границы и отступы.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                    </div>\r\n                </html>";

// Установите новый режим импорта блочных элементов HTML.
Aspose::Words::HtmlInsertOptions insertOptions = Aspose::Words::HtmlInsertOptions::PreserveBlocks;

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
builder->InsertHtml(html, insertOptions);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.PreserveBlocks.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
