---
title: "Aspose::Words::ChapterPageSeparator enum"
linktitle: "ChapterPageSeparator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ChapterPageSeparator enum. Definisce il carattere separatore che appare tra il capitolo e il numero di pagina in C++."
type: docs
weight: 84000
url: /it/cpp/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enum


Definisce il carattere separatore che appare tra il capitolo e il numero di pagina.

```cpp
enum class ChapterPageSeparator
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Trattino | 0 | Due punti. |
| Punto | 1 | Un punto. |
| Due punti | 2 | Due punti. |
| EmDash | 3 | Un trattino enfatizzato. |
| EnDash | 4 | Un trattino standard. |


## Esempi



Mostra come lavorare con i capitoli di pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_FirstSection()->get_PageSetup();

pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
pageSetup->set_ChapterPageSeparator(Aspose::Words::ChapterPageSeparator::Colon);
pageSetup->set_HeadingLevelForChapter(1);
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
