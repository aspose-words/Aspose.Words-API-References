---
title: "Aspose::Words::DocumentBuilder::get_Underline metodo"
linktitle: "get_Underline"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::get_Underline metodo. Ottiene/imposta il tipo di sottolineatura per il carattere corrente in C++."
type: docs
weight: 26000
url: /it/cpp/aspose.words/documentbuilder/get_underline/
---
## DocumentBuilder::get_Underline method


Ottiene/Imposta il tipo di sottolineatura per il carattere corrente.

```cpp
Aspose::Words::Underline Aspose::Words::DocumentBuilder::get_Underline()
```


## Esempi



Mostra come formattare il testo inserito da un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Dash);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(32);

// Il builder applica la formattazione al suo paragrafo corrente e a qualsiasi nuovo testo aggiunto successivamente.
builder->Writeln(u"Large, blue, and underlined text.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertUnderline.docx");
```

## Vedi anche

* Enum [Underline](../../underline/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
