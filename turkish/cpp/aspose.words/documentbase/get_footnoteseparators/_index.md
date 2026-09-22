---
title: "Aspose::Words::DocumentBase::get_FootnoteSeparators yöntemi"
linktitle: "get_FootnoteSeparators"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBase::get_FootnoteSeparators yöntemi. Belgedeki dipnot/sonnot ayırıcılarına C++'ta erişim sağlar."
type: docs
weight: 4500
url: /tr/cpp/aspose.words/documentbase/get_footnoteseparators/
---
## DocumentBase::get_FootnoteSeparators method


Belgede tanımlanan dipnot/dipnot ayırıcılarına erişim sağlar.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparatorCollection> Aspose::Words::DocumentBase::get_FootnoteSeparators() const
```


## Örnekler



Sonnot ayırıcıyı nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// Sonnot ayırıcıyı kaldır.
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


Dipnot ayırıcı biçimini nasıl yöneteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Dipnot ayırıcıyı hizala.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Ayrıca Bakınız

* Class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
