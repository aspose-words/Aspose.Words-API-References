---
title: "Metodo Aspose::Words::Font::get_ComplexScript"
linktitle: "get_ComplexScript"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_ComplexScript. Specifica se il contenuto di questo run deve essere trattato come testo a script complesso indipendentemente dai valori dei caratteri Unicode quando si determina la formattazione di questo run in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words/font/get_complexscript/
---
## Font::get_ComplexScript method


Specifica se il contenuto di questa sequenza deve essere trattato come testo a script complesso indipendentemente dai valori dei caratteri Unicode quando si determina la formattazione per questa sequenza.

```cpp
bool Aspose::Words::Font::get_ComplexScript()
```


## Esempi



Mostra come aggiungere testo che viene sempre trattato come script complesso.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_ComplexScript(true);

builder->Writeln(u"Text treated as complex script.");

doc->Save(get_ArtifactsDir() + u"Font.ComplexScript.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
