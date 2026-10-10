---
title: "Aspose::Words::ParagraphFormat::get_BaselineAlignment metodo"
linktitle: "get_BaselineAlignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphFormat::get_BaselineAlignment metodo. Ottiene o imposta la posizione verticale dei caratteri su una linea in C++."
type: docs
weight: 5500
url: /it/cpp/aspose.words/paragraphformat/get_baselinealignment/
---
## ParagraphFormat::get_BaselineAlignment method


Ottiene o imposta la posizione verticale dei font su una riga.

```cpp
Aspose::Words::BaselineAlignment Aspose::Words::ParagraphFormat::get_BaselineAlignment()
```


## Esempi



Mostra come impostare la posizione verticale dei caratteri su una riga.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();
if (format->get_BaselineAlignment() == Aspose::Words::BaselineAlignment::Auto)
{
    format->set_BaselineAlignment(Aspose::Words::BaselineAlignment::Top);
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphBaselineAlignment.docx");
```

## Vedi anche

* Enum [BaselineAlignment](../../baselinealignment/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
