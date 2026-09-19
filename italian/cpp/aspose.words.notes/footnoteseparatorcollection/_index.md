---
title: "Aspose::Words::Notes::FootnoteSeparatorCollection class"
linktitle: "FootnoteSeparatorCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Notes::FootnoteSeparatorCollection class. Fornisce accesso tipizzato ai nodi FootnoteSeparator di un documento in C++."
type: docs
weight: 3667
url: /it/cpp/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class


Fornisce accesso tipizzato ai nodi [FootnoteSeparator](../footnoteseparator/) di un documento.

```cpp
class FootnoteSeparatorCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [FootnoteSeparatorCollection](./footnoteseparatorcollection/)() |  |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::Notes::FootnoteSeparatorType) | Recupera un [FootnoteSeparator](../footnoteseparator/) del tipo specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come gestire il formato del separatore di nota a piè di pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Allinea il separatore di nota a piè di pagina.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Vedi anche

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
