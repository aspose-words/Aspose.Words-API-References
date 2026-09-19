---
title: "Aspose::Words::Font::get_StyleIdentifier metodo"
linktitle: "get_StyleIdentifier"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_StyleIdentifier. Ottiene o imposta l'identificatore di stile indipendente dalla locale dello stile di carattere applicato a questa formattazione in C++."
type: docs
weight: 43000
url: /it/cpp/aspose.words/font/get_styleidentifier/
---
## Font::get_StyleIdentifier method


Ottiene o imposta l'identificatore di stile indipendente dalla locale dello stile del carattere applicato a questa formattazione.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Font::get_StyleIdentifier()
```


## Esempi



Mostra come modificare lo stile del testo esistente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati due modi per fare riferimento agli stili.
// 1 -  Utilizzare il nome dello stile:
builder->get_Font()->set_StyleName(u"Emphasis");
builder->Writeln(u"Text originally in \"Emphasis\" style");

// 2 -  Utilizzare un identificatore di stile predefinito:
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::IntenseEmphasis);
builder->Writeln(u"Text originally in \"Intense Emphasis\" style");

// Converti tutti gli utilizzi di uno stile in un altro,
// usando i metodi sopra per fare riferimento agli stili vecchi e nuovi.
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    if (run->get_Font()->get_StyleName() == u"Emphasis")
    {
        run->get_Font()->set_StyleName(u"Strong");
    }

    if (run->get_Font()->get_StyleIdentifier() == Aspose::Words::StyleIdentifier::IntenseEmphasis)
    {
        run->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Strong);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.ChangeStyle.docx");
```

## Vedi anche

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
