---
title: "Aspose::Words::EmphasisMark enum"
linktitle: "EmphasisMark"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::EmphasisMark enum. Specifica i possibili tipi di segno di enfasi in C++."
type: docs
weight: 89000
url: /it/cpp/aspose.words/emphasismark/
---
## EmphasisMark enum


Specifica i possibili tipi di segno di enfasi.

```cpp
enum class EmphasisMark
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Nessun segno di enfasi. |
| OverSolidCircle | 1 | Il segno di enfasi è un cerchio nero pieno visualizzato sopra il testo. |
| OverComma | 2 | Il segno di enfasi è un carattere virgola visualizzato sopra il testo. |
| OverWhiteCircle | 3 | Il segno di enfasi è un cerchio bianco vuoto visualizzato sopra il testo. |
| UnderSolidCircle | 4 | Il segno di enfasi è un cerchio nero pieno visualizzato sotto il testo. |


## Esempi



Mostra come aggiungere un carattere aggiuntivo visualizzato sopra/sotto il glyph-character.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Possibili tipi di segno di enfasi:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(get_ArtifactsDir() + u"Fonts.SetEmphasisMark.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
