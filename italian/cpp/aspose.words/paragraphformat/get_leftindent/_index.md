---
title: "Aspose::Words::ParagraphFormat::get_LeftIndent metodo"
linktitle: "get_LeftIndent"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphFormat::get_LeftIndent metodo. Ottiene o imposta il valore (in punti) che rappresenta l'indentazione sinistra per il paragrafo in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words/paragraphformat/get_leftindent/
---
## ParagraphFormat::get_LeftIndent method


Ottiene o imposta il valore (in punti) che rappresenta il rientro sinistro per il paragrafo.

```cpp
double Aspose::Words::ParagraphFormat::get_LeftIndent()
```


## Esempi



Mostra come configurare la formattazione dei paragrafi per creare testo fuori centro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Centra tutto il testo che il document builder scrive e imposta le indentazioni.
// La configurazione di indentazione qui sotto creerà un blocco di testo che si posizionerà in modo asimmetrico sulla pagina.
// Il "centro" a cui allineiamo il testo sarà il mezzo del corpo del testo, non il mezzo della pagina.
System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
paragraphFormat->set_LeftIndent(100);
paragraphFormat->set_RightIndent(50);
paragraphFormat->set_SpaceAfter(25);

builder->Writeln(u"This paragraph demonstrates how left and right indentation affects word wrapping.");
builder->Writeln(u"The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetParagraphFormatting.docx");
```

## Vedi anche

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
