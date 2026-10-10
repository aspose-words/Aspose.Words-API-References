---
title: "Aspose::Words::TextOrientation enum"
linktitle: "TextOrientation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TextOrientation enum. Specifica l'orientamento del testo su una pagina, in una cella di tabella o in un frame di testo in C++."
type: docs
weight: 124000
url: /it/cpp/aspose.words/textorientation/
---
## TextOrientation enum


Specifica l'orientamento del testo su una pagina, in una cella di tabella o in un riquadro di testo.

```cpp
enum class TextOrientation
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Orizzontale | 0 | Il testo è disposto orizzontalmente (lr-tb). |
| Verso il basso | 1 | Il testo è ruotato di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl). |
| Verso l'alto | 3 | Il testo è ruotato di 90 gradi verso sinistra per apparire dal basso verso l'alto (bt-lr). |
| HorizontalRotatedFarEast | 4 | Il testo è disposto orizzontalmente, ma i caratteri dell'Estremo Oriente sono ruotati di 90 gradi verso sinistra (lr-tb-v). |
| VerticalFarEast | 5 | I caratteri dell'Estremo Oriente appaiono verticali, gli altri testi sono ruotati di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl-v). |
| VerticalRotatedFarEast | 7 | I caratteri dell'Estremo Oriente appaiono verticali, gli altri testi sono ruotati di 90 gradi verso destra per apparire dall'alto verso il basso verticalmente, poi da sinistra a destra orizzontalmente (tb-lr-v). |


## Esempi



Mostra come creare una tabella formattata 2x2.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// Durante la creazione della tabella, il costruttore di documenti applicherà i valori delle proprietà RowFormat/CellFormat correnti
// alla riga/cella corrente in cui si trova il cursore e a tutte le nuove righe/celle man mano che le crea.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Le righe e le celle aggiunte in precedenza non sono retroattivamente influenzate dalle modifiche al formato del costruttore.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
