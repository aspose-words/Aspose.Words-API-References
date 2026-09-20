---
title: "Aspose::Words::Document::UpdateActualReferenceMarks метод"
linktitle: "UpdateActualReferenceMarks"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::UpdateActualReferenceMarks метод. Обновляет свойство ActualReferenceMark всех сносок и концевых сносок в документе на C++."
type: docs
weight: 95500
url: /ru/cpp/aspose.words/document/updateactualreferencemarks/
---
## Document::UpdateActualReferenceMarks method


Обновляет свойство [ActualReferenceMark](../../../aspose.words.notes/footnote/get_actualreferencemark/) всех сносок и концевых сносок в документе.

```cpp
void Aspose::Words::Document::UpdateActualReferenceMarks()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
