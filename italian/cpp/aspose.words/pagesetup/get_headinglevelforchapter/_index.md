---
title: "Aspose::Words::PageSetup::get_HeadingLevelForChapter metodo"
linktitle: "get_HeadingLevelForChapter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PageSetup::get_HeadingLevelForChapter metodo. Ottiene o imposta lo stile di livello di intestazione che viene applicato ai titoli dei capitoli nel documento in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words/pagesetup/get_headinglevelforchapter/
---
## PageSetup::get_HeadingLevelForChapter method


Ottiene o imposta lo stile di livello di intestazione applicato ai titoli dei capitoli nel documento.

```cpp
int32_t Aspose::Words::PageSetup::get_HeadingLevelForChapter()
```

## Note


Può essere un numero da 0 a 9. 0 significa nessun numero di capitolo se applicato al numero di pagina.

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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
