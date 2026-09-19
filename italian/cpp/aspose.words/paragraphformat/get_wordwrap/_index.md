---
title: "Metodo Aspose::Words::ParagraphFormat::get_WordWrap"
linktitle: "get_WordWrap"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ParagraphFormat::get_WordWrap. Se questa proprietà è false, il testo latino al centro di una parola può essere interrotto per il paragrafo corrente. Altrimenti il testo latino è interrotto per parole intere in C++."
type: docs
weight: 42000
url: /it/cpp/aspose.words/paragraphformat/get_wordwrap/
---
## ParagraphFormat::get_WordWrap method


Se questa proprietà è **false**, il testo latino al centro di una parola può essere interrotto per il paragrafo corrente. Altrimenti il testo latino è interrotto per parole intere.

```cpp
bool Aspose::Words::ParagraphFormat::get_WordWrap()
```


## Esempi



Mostra come impostare proprietà speciali per la tipografia asiatica.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_FarEastLineBreakControl(true);
format->set_WordWrap(false);
format->set_HangingPunctuation(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.AsianTypographyProperties.docx");
```

## Vedi anche

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
