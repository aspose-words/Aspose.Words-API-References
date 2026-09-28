---
title: "Метод Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase"
linktitle: "get_HyperlinkBase"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase. Указывает базовую строку, используемую для оценки относительных гиперссылок в этом документе в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkbase/
---
## BuiltInDocumentProperties::get_HyperlinkBase method


Указывает базовую строку, используемую для оценки относительных гиперссылок в этом документе.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase()
```

## Примечания


Aspose.Words не использует это свойство.

## Примеры



Показывает, как сохранить базовую часть гиперссылки в свойствах документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте относительную гиперссылку на документ в локальной файловой системе с именем \"Document.docx\".
// Щелчок по ссылке в Microsoft Word откроет указанный документ, если он доступен.
builder->InsertHyperlink(u"Relative hyperlink", u"Document.docx", false);

// Эта ссылка относительная. Если в той же папке нет файла \"Document.docx\"
// как и документ, содержащий эту ссылку, ссылка будет сломана.
ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"Document.docx"));
doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Документ, к которому мы пытаемся создать ссылку, находится в другом каталоге, чем тот, в котором мы планируем сохранить документ.
// Мы могли бы исправить такие ссылки, указав абсолютное имя файла в каждой из них.
// В качестве альтернативы мы могли бы задать базовую ссылку, которую будет использовать каждая гиперссылка с относительным именем файла
// будет добавлена к её ссылке при щелчке.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();
properties->set_HyperlinkBase(get_MyDir());

ASSERT_TRUE(System::IO::File::Exists(properties->get_HyperlinkBase() + (System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(doc->get_Range()->get_Fields()->idx_get(0)))->get_Address()));

doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

## См. также

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
