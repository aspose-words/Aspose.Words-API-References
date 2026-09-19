---
title: "Aspose::Words::LineSpacingRule enum"
linktitle: "LineSpacingRule"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::LineSpacingRule enum. Specifica i valori di interlinea per un paragrafo in C++."
type: docs
weight: 95000
url: /it/cpp/aspose.words/linespacingrule/
---
## LineSpacingRule enum


Specifica i valori di interlinea per un paragrafo.

```cpp
enum class LineSpacingRule
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| AtLeast | 0 | L'interlinea può essere maggiore o uguale, ma mai inferiore, al valore specificato nella proprietà [LineSpacing](../paragraphformat/get_linespacing/). |
| Exactly | 1 | L'interlinea non cambia mai dal valore specificato nella proprietà [LineSpacing](../paragraphformat/get_linespacing/), anche se nel paragrafo viene utilizzato un carattere più grande. |
| Multiple | 2 | L'interlinea è specificata nella proprietà [LineSpacing](../paragraphformat/get_linespacing/) come numero di linee. Una linea equivale a 12 punti. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
