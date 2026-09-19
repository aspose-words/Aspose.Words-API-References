---
title: "Metodo Aspose::Words::Font::get_EmphasisMark"
linktitle: "get_EmphasisMark"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_EmphasisMark. Ottiene o imposta il segno di enfasi applicato a questa formattazione in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words/font/get_emphasismark/
---
## Font::get_EmphasisMark method


Ottiene o imposta il segno di enfasi applicato a questa formattazione.

```cpp
Aspose::Words::EmphasisMark Aspose::Words::Font::get_EmphasisMark()
```


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

* Enum [EmphasisMark](../../emphasismark/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
