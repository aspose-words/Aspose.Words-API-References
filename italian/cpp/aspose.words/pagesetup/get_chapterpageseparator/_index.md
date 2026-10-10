---
title: "Metodo Aspose::Words::PageSetup::get_ChapterPageSeparator"
linktitle: "get_ChapterPageSeparator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::PageSetup::get_ChapterPageSeparator. Ottiene o imposta il carattere separatore che appare tra il numero del capitolo e il numero della pagina in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/pagesetup/get_chapterpageseparator/
---
## PageSetup::get_ChapterPageSeparator method


Ottiene o imposta il carattere separatore che appare tra il numero del capitolo e il numero di pagina.

```cpp
Aspose::Words::ChapterPageSeparator Aspose::Words::PageSetup::get_ChapterPageSeparator()
```

## Note


Prima di poter creare numeri di pagina che includono i numeri dei capitoli, le intestazioni del documento devono avere applicato un formato di struttura numerata.

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

* Enum [ChapterPageSeparator](../../chapterpageseparator/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
