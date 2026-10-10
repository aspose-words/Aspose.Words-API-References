---
title: "Aspose::Words::Paragraph::get_IsFormatRevision metodo"
linktitle: "get_IsFormatRevision"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Paragraph::get_IsFormatRevision. Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre il tracciamento delle modifiche era abilitato in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/paragraph/get_isformatrevision/
---
## Paragraph::get_IsFormatRevision method


Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre il tracciamento delle modifiche era abilitato.

```cpp
bool Aspose::Words::Paragraph::get_IsFormatRevision()
```


## Esempi



Mostra come verificare se un paragrafo è una revisione di formattazione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Format revision.docx");

// Questo paragrafo è una revisione "Formato", che si verifica quando modifichiamo la formattazione del testo esistente.
// mentre tracciamo le revisioni in Microsoft Word tramite "Review" -> "Track changes".
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_IsFormatRevision());
```

## Vedi anche

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
