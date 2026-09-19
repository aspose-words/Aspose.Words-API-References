---
title: "Metodo Aspose::Words::Font::get_AutoColor"
linktitle: "get_AutoColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_AutoColor. Restituisce il colore calcolato attuale del testo (nero o bianco) da utilizzare per ''auto color''. Se il colore non è ''auto'' restituisce Color in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/font/get_autocolor/
---
## Font::get_AutoColor method


Restituisce il colore calcolato attuale del testo (nero o bianco) da utilizzare per 'auto color'. Se il colore non è 'auto' restituisce [Color](../get_color/).

```cpp
System::Drawing::Color Aspose::Words::Font::get_AutoColor()
```

## Note


Quando il testo ha 'colore automatico', il colore reale del testo viene calcolato automaticamente in modo che sia leggibile sul colore di sfondo. Modificando il colore di sfondo, il colore del testo si cambierà automaticamente in nero o bianco in MS Word per massimizzare la leggibilità.

## Esempi



Mostra come migliorare la leggibilità selezionando automaticamente il colore del testo in base alla luminosità dello sfondo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Se l'oggetto Font di un run non specifica il colore del testo, lo farà automaticamente
// seleziona nero o bianco a seconda del colore di sfondo.
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());

// Il colore predefinito per il testo è il nero. Se il colore dello sfondo è scuro, il testo nero sarà difficile da vedere.
// Per risolvere questo problema, la proprietà AutoColor visualizzerà questo testo in bianco.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"The text color automatically chosen for this run is white.");

ASSERT_EQ(System::Drawing::Color::get_White().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

// Se cambiamo lo sfondo in un colore chiaro, il nero sarà un
// colore del testo più adatto rispetto al bianco, così il colore automatico lo visualizzerà in nero.
builder->get_Font()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());

builder->Writeln(u"The text color automatically chosen for this run is black.");

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_AutoColor().ToArgb());

doc->Save(get_ArtifactsDir() + u"Font.SetFontAutoColor.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
