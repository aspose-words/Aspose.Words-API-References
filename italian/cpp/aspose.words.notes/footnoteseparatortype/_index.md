---
title: "Aspose::Words::Notes::FootnoteSeparatorType enum"
linktitle: "FootnoteSeparatorType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Notes::FootnoteSeparatorType enum. Specifica il tipo del separatore di nota a piè di pagina/fine nota in C++."
type: docs
weight: 6500
url: /it/cpp/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enum


Specifica il tipo del separatore di nota a piè di pagina/note finale.

```cpp
enum class FootnoteSeparatorType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| FootnoteSeparator | 0 | Separatore tra il testo principale e il testo della nota a piè di pagina. |
| FootnoteContinuationSeparator | 1 | Stampato sopra il testo della nota a piè di pagina su una pagina quando il testo deve essere continuato da una pagina precedente. |
| FootnoteContinuationNotice | 2 | Stampato sotto il testo della nota a piè di pagina su una pagina quando il testo della nota a piè di pagina deve essere continuato su una pagina successiva. |
| EndnoteSeparator | 3 | Separatore tra il testo principale e il testo della nota finale. |
| EndnoteContinuationSeparator | 4 | Stampato sopra il testo della nota finale su una pagina quando il testo deve essere continuato da una pagina precedente. |
| EndnoteContinuationNotice | 5 | Stampato sotto il testo della nota finale su una pagina quando il testo della nota finale deve essere continuato su una pagina successiva. |


## Esempi



Mostra come rimuovere il separatore di nota finale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// Rimuovi il separatore di nota finale.
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


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
