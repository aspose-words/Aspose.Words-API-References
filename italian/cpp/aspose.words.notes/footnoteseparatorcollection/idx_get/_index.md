---
title: "Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get metodo"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get metodo. Recupera un FootnoteSeparator del tipo specificato in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.notes/footnoteseparatorcollection/idx_get/
---
## FootnoteSeparatorCollection::idx_get method


Recupera un [FootnoteSeparator](../../footnoteseparator/) del tipo specificato.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get(Aspose::Words::Notes::FootnoteSeparatorType separatorType)
```


## Esempi



Mostra come gestire il formato del separatore di nota a piè di pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Allinea il separatore di nota a piè di pagina.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Vedi anche

* Class [FootnoteSeparator](../../footnoteseparator/)
* Enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* Class [FootnoteSeparatorCollection](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
