---
title: "Metodo Aspose::Words::PlainTextDocument::get_Text"
linktitle: "get_Text"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::PlainTextDocument::get_Text. Ottiene il contenuto testuale del documento concatenato come stringa in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/plaintextdocument/get_text/
---
## PlainTextDocument::get_Text method


Ottiene il contenuto testuale del documento concatenato in una stringa.

```cpp
System::String Aspose::Words::PlainTextDocument::get_Text() const
```


## Esempi



Mostra come caricare il contenuto di un documento Microsoft Word in testo semplice.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## Vedi anche

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
