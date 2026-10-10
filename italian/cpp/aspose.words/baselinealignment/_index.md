---
title: "Aspose::Words::BaselineAlignment enum"
linktitle: "BaselineAlignment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BaselineAlignment enum. Specifica la posizione verticale dei caratteri su una riga in C++."
type: docs
weight: 80500
url: /it/cpp/aspose.words/baselinealignment/
---
## BaselineAlignment enum


Specifica la posizione verticale del font su una riga.

```cpp
enum class BaselineAlignment
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Superiore | 0 | Allinea lungo la parte superiore di ogni carattere. |
| Centro | 1 | Allinea i punti centrali di ogni carattere. |
| Linea di base | 2 | Allinea alla linea di base del paragrafo. |
| Inferiore | 3 | Allinea alla parte inferiore di ogni carattere. |
| Auto | 4 | La linea di base è regolata automaticamente. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
