---
title: "Aspose::Words::Document::get_PunctuationKerning метод"
linktitle: "get_PunctuationKerning"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_PunctuationKerning. Указывает, применяется ли кернинг как к латинскому тексту, так и к пунктуации в C++."
type: docs
weight: 44500
url: /ru/cpp/aspose.words/document/get_punctuationkerning/
---
## Document::get_PunctuationKerning method


Указывает, применяется ли кернинг к латинскому тексту и пунктуации.

```cpp
bool Aspose::Words::Document::get_PunctuationKerning()
```


## Примеры



Показывает, как работать с кернингом, применяемым как к латинскому тексту, так и к пунктуации.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_TRUE(doc->get_PunctuationKerning());
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
