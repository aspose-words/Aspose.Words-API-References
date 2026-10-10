---
title: "Metodo Aspose::Words::Font::get_Shadow"
linktitle: "get_Shadow"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_Shadow. Vero se il font è formattato come ombreggiato in C++."
type: docs
weight: 35000
url: /it/cpp/aspose.words/font/get_shadow/
---
## Font::get_Shadow method


True se il font è formattato come ombreggiato.

```cpp
bool Aspose::Words::Font::get_Shadow()
```


## Esempi



Mostra come creare una sequenza di testo formattata con un'ombreggiatura.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Imposta il flag Shadow per applicare un effetto di ombra offset,
// facendo sembrare le lettere sospese sopra la pagina.
builder->get_Font()->set_Shadow(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has a shadow.");

doc->Save(get_ArtifactsDir() + u"Font.Shadow.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
