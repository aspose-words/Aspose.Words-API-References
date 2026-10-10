---
title: "Aspose::Words::ParagraphFormat::get_LineSpacingRule metodo"
linktitle: "get_LineSpacingRule"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphFormat::get_LineSpacingRule metodo. Ottiene o imposta l'interlinea per il paragrafo in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words/paragraphformat/get_linespacingrule/
---
## ParagraphFormat::get_LineSpacingRule method


Ottiene o imposta l'interlinea per il paragrafo.

```cpp
Aspose::Words::LineSpacingRule Aspose::Words::ParagraphFormat::get_LineSpacingRule()
```


## Esempi



Mostra come lavorare con l'interlinea.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportate tre regole di interlinea che possiamo definire usando il
// proprietà "LineSpacingRule" del paragrafo per configurare la spaziatura tra i paragrafi.
// 1 -  Imposta una quantità minima di spaziatura.
// Questo fornirà un'imbottitura verticale alle linee di testo di qualsiasi dimensione
// che è troppo piccola per mantenere l'altezza minima della linea.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::AtLeast);
builder->get_ParagraphFormat()->set_LineSpacing(20);

builder->Writeln(u"Minimum line spacing of 20.");
builder->Writeln(u"Minimum line spacing of 20.");

// 2 -  Imposta spaziatura esatta.
// L'uso di dimensioni del carattere troppo grandi per la spaziatura troncherà il testo.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Exactly);
builder->get_ParagraphFormat()->set_LineSpacing(5);

builder->Writeln(u"Line spacing of exactly 5.");
builder->Writeln(u"Line spacing of exactly 5.");

// 3 -  Imposta la spaziatura come multiplo della spaziatura di linea predefinita, che è di 12 punti per impostazione predefinita.
// Questo tipo di spaziatura si adatterà a diverse dimensioni del carattere.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Multiple);
builder->get_ParagraphFormat()->set_LineSpacing(18);

builder->Writeln(u"Line spacing of 1.5 default lines.");
builder->Writeln(u"Line spacing of 1.5 default lines.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LineSpacing.docx");
```

## Vedi anche

* Enum [LineSpacingRule](../../linespacingrule/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
