---
title: "Metodo Aspose::Words::Font::get_Hidden"
linktitle: "get_Hidden"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_Hidden. True se il carattere è formattato come testo nascosto in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words/font/get_hidden/
---
## Font::get_Hidden method


Vero se il carattere è formattato come testo nascosto.

```cpp
bool Aspose::Words::Font::get_Hidden()
```


## Esempi



Mostra come creare una sequenza di testo nascosto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Con l'opzione Hidden impostata su true, qualsiasi testo creato con questo oggetto Font sarà invisibile nel documento.
// Non vedremo né evidenzieremo il testo nascosto a meno che non abilitiamo l'opzione "Hidden text"
// trovato in Microsoft Word tramite "File" -> "Options" -> "Display". Il testo sarà comunque presente,
// e potremo accedere a questo testo programmaticamente.
// Non è consigliato utilizzare questo metodo per nascondere informazioni sensibili.
builder->get_Font()->set_Hidden(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text will not be visible in the document.");

doc->Save(get_ArtifactsDir() + u"Font.Hidden.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
