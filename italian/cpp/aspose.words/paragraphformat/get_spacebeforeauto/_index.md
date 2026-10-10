---
title: "Metodo Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto"
linktitle: "get_SpaceBeforeAuto"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto. True se la quantità di spaziatura prima del paragrafo è impostata automaticamente in C++."
type: docs
weight: 34000
url: /it/cpp/aspose.words/paragraphformat/get_spacebeforeauto/
---
## ParagraphFormat::get_SpaceBeforeAuto method


Vero se la quantità di spaziatura prima del paragrafo è impostata automaticamente.

```cpp
bool Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto()
```

## Note


Quando impostato su **true**, sovrascrive l'effetto di [SpaceBefore](../get_spacebefore/).

Quando imposti lo Space Before e lo Space After del paragrafo su Auto, **Microsoft** Word aggiunge automaticamente una spaziatura di 14 punti tra i paragrafi secondo le seguenti regole:

* Normally, spacing is added after all paragraphs.
* In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
* In a nested bulleted or numbered list spacing is not added.
* Spacing is normally added after a table.
* Spacing is not added after a table if it is the last block in a table cell.
* Spacing is not added after the last paragraph in a table cell.



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

## Vedi anche

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
