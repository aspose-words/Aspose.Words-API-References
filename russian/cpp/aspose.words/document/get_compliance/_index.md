---
title: "Aspose::Words::Document::get_Compliance метод"
linktitle: "get_Compliance"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::get_Compliance метод. Получает версию соответствия OOXML, определённую из содержимого загруженного документа. Имеет смысл только для документов OOXML в C++."
type: docs
weight: 17000
url: /ru/cpp/aspose.words/document/get_compliance/
---
## Document::get_Compliance method


Получает версию соответствия OOXML, определённую из содержимого загруженного документа. Имеет смысл только для документов OOXML.

```cpp
Aspose::Words::Saving::OoxmlCompliance Aspose::Words::Document::get_Compliance()
```

## Примечания


Если вы создали новый пустой документ или загрузили не OOXML документ, возвращается значение [Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/).

## Примеры



Показывает, как прочитать версию соответствия Open Office XML загруженного документа.
```cpp
// Версия соответствия различается в зависимости от документов, созданных разными версиями Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.doc");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Ecma376_2006);

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_EQ(doc->get_Compliance(), Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);
```

## См. также

* Enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
