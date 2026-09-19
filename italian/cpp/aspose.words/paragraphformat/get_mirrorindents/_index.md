---
title: "Aspose::Words::ParagraphFormat::get_MirrorIndents metodo"
linktitle: "get_MirrorIndents"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ParagraphFormat::get_MirrorIndents. Ottiene o imposta un flag che indica se le rientranze sinistra e destra hanno la stessa larghezza in C++."
type: docs
weight: 24500
url: /it/cpp/aspose.words/paragraphformat/get_mirrorindents/
---
## ParagraphFormat::get_MirrorIndents method


Ottiene o imposta un flag che indica se i rientri sinistro e destro hanno la stessa larghezza.

```cpp
bool Aspose::Words::ParagraphFormat::get_MirrorIndents()
```


## Esempi



Mostra come rendere le rientranze sinistra e destra uguali.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();

format->set_MirrorIndents(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.MirrorIndents.docx");
```

## Vedi anche

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
