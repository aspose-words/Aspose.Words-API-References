---
title: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark метод"
linktitle: "get_ActualReferenceMark"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark метод. Получает фактический текст метки ссылки, отображаемой в документе для этой сноски в C++."
type: docs
weight: 3834
url: /ru/cpp/aspose.words.notes/footnote/get_actualreferencemark/
---
## Footnote::get_ActualReferenceMark method


Получает фактический текст ссылочного знака, отображаемого в документе для этой сноски.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ActualReferenceMark()
```


## Примеры



Показывает, как получить фактическую метку ссылки сноски.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## См. также

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
