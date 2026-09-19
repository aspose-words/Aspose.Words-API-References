---
title: "Metodo Aspose::Words::Paragraph::get_BreakIsStyleSeparator"
linktitle: "get_BreakIsStyleSeparator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Paragraph::get_BreakIsStyleSeparator. True se questa interruzione di paragrafo è un Separatore di Stile. Un separatore di stile consente a un paragrafo di essere composto da parti con stili di paragrafo diversi in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/paragraph/get_breakisstyleseparator/
---
## Paragraph::get_BreakIsStyleSeparator method


True se questa interruzione di paragrafo è un Separatore di [Style](../../style/). Un separatore di stile consente a un paragrafo di essere composto da parti con stili di paragrafo diversi.

```cpp
bool Aspose::Words::Paragraph::get_BreakIsStyleSeparator()
```


## Esempi



Mostra come scrivere testo sulla stessa riga di un'intestazione del TOC senza che compaia nel TOC.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertTableOfContents(u"\\o \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Inserisci un paragrafo con uno stile che il TOC riconoscerà come voce.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

// Entrambe queste stringhe sono nello stesso paragrafo e quindi appariranno nella stessa voce del TOC.
builder->Write(u"Heading 1. ");
builder->Write(u"Will appear in the TOC. ");

// Se inseriamo un separatore di stile, possiamo scrivere più testo nello stesso paragrafo
// e usare uno stile diverso senza comparire nel TOC.
// Se utilizziamo uno stile di tipo intestazione dopo il separatore, possiamo generare più voci del TOC da una singola riga di testo del documento.
builder->InsertStyleSeparator();
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Quote);
builder->Write(u"Won't appear in the TOC. ");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_BreakIsStyleSeparator());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Paragraph.BreakIsStyleSeparator.docx");
```

## Vedi anche

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
