---
title: "Aspose::Words::Document::RemoveBlankPages Methode"
linktitle: "RemoveBlankPages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::RemoveBlankPages Methode. Entfernt leere Seiten aus dem Dokument in C++."
type: docs
weight: 67500
url: /de/cpp/aspose.words/document/removeblankpages/
---
## Document::RemoveBlankPages method


Entfernt leere Seiten aus dem Dokument.

```cpp
System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::Document::RemoveBlankPages()
```


### ReturnValue

Liste von Seitenzahlen wurde als leer betrachtet und entfernt.

## Beispiele



Zeigt, wie leere Seiten aus dem Dokument entfernt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Blank pages.docx");
ASSERT_EQ(2, doc->get_PageCount());
doc->RemoveBlankPages();
doc->UpdatePageLayout();
ASSERT_EQ(1, doc->get_PageCount());
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
