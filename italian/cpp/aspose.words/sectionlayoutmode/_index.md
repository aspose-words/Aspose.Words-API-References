---
title: "Aspose::Words::SectionLayoutMode enum"
linktitle: "SectionLayoutMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::SectionLayoutMode enum. Specifica la modalità di layout per una sezione consentendo di definire il comportamento della griglia del documento in C++."
type: docs
weight: 115000
url: /it/cpp/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enum


Specifica la modalità di layout per una sezione consentendo di definire il comportamento della griglia del documento.

```cpp
enum class SectionLayoutMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Default | 0 | Specifica che nessuna griglia del documento deve essere applicata al contenuto della sezione corrispondente nel documento. |
| Griglia | 1 | Specifica che la sezione corrispondente deve avere sia la spaziatura aggiuntiva delle righe sia la spaziatura dei caratteri aggiunta a ogni riga e carattere al suo interno, al fine di mantenere un numero specifico di righe per pagina e di caratteri per riga. I caratteri non saranno allineati automaticamente alle linee della griglia durante la digitazione. |
| LineGrid | 2 | Specifica che la sezione corrispondente deve avere una spaziatura aggiuntiva delle righe aggiunta a ogni riga al suo interno, al fine di mantenere il numero specificato di righe per pagina. |
| SnapToChars | 3 | Specifica che la sezione corrispondente deve avere sia la spaziatura aggiuntiva delle righe sia la spaziatura dei caratteri aggiunta a ogni riga e carattere al suo interno, al fine di mantenere un numero specifico di righe per pagina e di caratteri per riga. I caratteri saranno allineati automaticamente alle linee della griglia durante la digitazione. |


## Esempi



Mostra come specificare un valore per il numero di caratteri che ogni riga può contenere.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Abilita il pitching e poi usalo per impostare il numero di caratteri per riga in questa sezione.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::Grid);
builder->get_PageSetup()->set_CharactersPerLine(10);

// Il numero di caratteri dipende anche dalla dimensione del carattere.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(20);

ASSERT_EQ(8, doc->get_FirstSection()->get_PageSetup()->get_CharactersPerLine());

builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CharactersPerLine.docx");
```


Mostra come specificare un limite per il numero di righe che ogni pagina può contenere.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Abilita il pitching e poi usalo per impostare il numero di righe per pagina in questa sezione.
// Una dimensione del carattere sufficientemente grande sposterà alcune righe nella pagina successiva per evitare la sovrapposizione dei caratteri.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
