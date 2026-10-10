---
title: "Aspose::Words::ParagraphFormat::get_SpaceAfter metodo"
linktitle: "get_SpaceAfter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphFormat::get_SpaceAfter metodo. Ottiene o imposta la quantità di spaziatura (in punti) dopo il paragrafo in C++."
type: docs
weight: 31000
url: /it/cpp/aspose.words/paragraphformat/get_spaceafter/
---
## ParagraphFormat::get_SpaceAfter method


Ottiene o imposta la quantità di spaziatura (in punti) dopo il paragrafo.

```cpp
double Aspose::Words::ParagraphFormat::get_SpaceAfter()
```

## Note


Non ha alcun effetto quando [SpaceAfterAuto](../get_spaceafterauto/) è **true**.

I valori validi vanno da 0 a 1584 inclusi.

## Esempi



Mostra come impostare la spaziatura automatica dei paragrafi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Applica una grande quantità di spaziatura prima e dopo i paragrafi che questo builder creerà.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Imposta questi flag su "true" per applicare la spaziatura automatica,
// ignorando efficacemente la spaziatura nelle proprietà che abbiamo impostato sopra.
// Lasciandoli impostati su "false" verrà applicata la nostra spaziatura personalizzata del paragrafo.
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// Inserisci due paragrafi che avranno spaziatura sopra e sotto di essi e salva il documento.
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```


Mostra come applicare nessuna spaziatura tra paragrafi con lo stesso stile.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Applica una grande quantità di spaziatura prima e dopo i paragrafi che questo builder creerà.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Imposta il flag "NoSpaceBetweenParagraphsOfSameStyle" su "true" per applicare
// nessuna spaziatura tra paragrafi con lo stesso stile, il che raggrupperà paragrafi simili.
// Lascia il flag "NoSpaceBetweenParagraphsOfSameStyle" su "false"
// per applicare uniformemente la spaziatura a ogni paragrafo.
builder->get_ParagraphFormat()->set_NoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

## Vedi anche

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
