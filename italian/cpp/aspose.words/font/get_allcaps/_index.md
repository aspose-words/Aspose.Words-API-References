---
title: "Aspose::Words::Font::get_AllCaps metodo"
linktitle: "get_AllCaps"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_AllCaps. Vero se il carattere è formattato tutto in maiuscolo in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/font/get_allcaps/
---
## Font::get_AllCaps method


Vero se il carattere è formattato tutto in maiuscolo.

```cpp
bool Aspose::Words::Font::get_AllCaps()
```


## Esempi



Mostra come formattare un run per visualizzare il suo contenuto in maiuscolo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Ci sono due modi per far visualizzare a un run il suo testo in minuscolo in maiuscolo senza modificarne il contenuto.
// 1 -  Imposta il flag AllCaps per visualizzare tutti i caratteri in maiuscolo regolare:
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"all capitals");
run->get_Font()->set_AllCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

para = System::ExplicitCast<Aspose::Words::Paragraph>(para->get_ParentNode()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));

// 2 -  Imposta il flag SmallCaps per visualizzare tutti i caratteri in maiuscole piccole:
// Se un carattere è minuscolo, apparirà nella sua forma maiuscola
// ma avrà la stessa altezza del minuscolo (l'x-height del font).
// I caratteri che erano originariamente in maiuscolo appariranno allo stesso modo.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Small Capitals");
run->get_Font()->set_SmallCaps(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.Caps.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
