---
title: "Aspose::Words::Font::get_StrikeThrough metodo"
linktitle: "get_StrikeThrough"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_StrikeThrough metodo. Vero se il carattere è formattato come barrato in C++."
type: docs
weight: 41000
url: /it/cpp/aspose.words/font/get_strikethrough/
---
## Font::get_StrikeThrough method


True se il font è formattato come testo barrato.

```cpp
bool Aspose::Words::Font::get_StrikeThrough()
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
