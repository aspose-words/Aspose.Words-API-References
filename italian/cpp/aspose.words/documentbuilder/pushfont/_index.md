---
title: "Aspose::Words::DocumentBuilder::PushFont metodo"
linktitle: "PushFont"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::PushFont metodo. Salva la formattazione dei caratteri corrente nello stack in C++."
type: docs
weight: 63000
url: /it/cpp/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder::PushFont method


Salva la formattazione dei caratteri corrente nello stack.

```cpp
void Aspose::Words::DocumentBuilder::PushFont()
```


## Esempi



Mostra come utilizzare lo stack di formattazione di un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Imposta la formattazione del carattere, poi scrivi il testo che precede il collegamento ipertestuale.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Conserva la nostra configurazione di formattazione corrente nello stack.
builder->PushFont();

// Modifica la formattazione corrente del builder applicando un nuovo stile.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Ripristina la formattazione del carattere che abbiamo salvato in precedenza e rimuovi l'elemento dallo stack.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```

## Vedi anche

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
