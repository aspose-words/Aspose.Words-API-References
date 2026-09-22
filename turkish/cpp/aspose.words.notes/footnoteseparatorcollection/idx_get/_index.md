---
title: "Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get yöntemi"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get yöntemi. C++'da belirtilen türde bir FootnoteSeparator alır."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.notes/footnoteseparatorcollection/idx_get/
---
## FootnoteSeparatorCollection::idx_get method


Belirtilen türde bir [FootnoteSeparator](../../footnoteseparator/) alır.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get(Aspose::Words::Notes::FootnoteSeparatorType separatorType)
```


## Örnekler



Dipnot ayırıcı biçimini nasıl yöneteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Dipnot ayırıcıyı hizala.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Ayrıca Bakınız

* Class [FootnoteSeparator](../../footnoteseparator/)
* Enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* Class [FootnoteSeparatorCollection](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
