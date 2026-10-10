---
title: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl metodo"
linktitle: "get_FarEastLineBreakControl"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl metodo. Ottiene o imposta un flag che indica se le regole di interruzione di riga dell'Asia orientale sono applicate al paragrafo corrente in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/paragraphformat/get_fareastlinebreakcontrol/
---
## ParagraphFormat::get_FarEastLineBreakControl method


Ottiene o imposta un flag che indica se le regole di interruzione di riga dell'Asia orientale sono applicate al paragrafo corrente.

```cpp
bool Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl()
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
