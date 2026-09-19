---
title: "Metodo Aspose::Words::Font::get_DoubleStrikeThrough"
linktitle: "get_DoubleStrikeThrough"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_DoubleStrikeThrough. Vero se il carattere è formattato come testo barrato doppio in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/font/get_doublestrikethrough/
---
## Font::get_DoubleStrikeThrough method


Vero se il carattere è formattato con doppia barratura.

```cpp
bool Aspose::Words::Font::get_DoubleStrikeThrough()
```


## Esempi



Mostra come aggiungere una barra di cancellazione al testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Text with a single-line strikethrough.");
run->get_Font()->set_StrikeThrough(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

run = System::MakeObject<Aspose::Words::Run>(doc, u"Text with a double-line strikethrough.");
run->get_Font()->set_DoubleStrikeThrough(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.StrikeThrough.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
