---
title: "Aspose::Words::HeightRule enum"
linktitle: "HeightRule"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::HeightRule enum. Specifica la regola per determinare l'altezza di un oggetto in C++."
type: docs
weight: 91000
url: /it/cpp/aspose.words/heightrule/
---
## HeightRule enum


Specifica la regola per determinare l'altezza di un oggetto.

```cpp
enum class HeightRule
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| AtLeast | 0 | L'altezza sarà almeno l'altezza specificata in punti. Crescerà, se necessario, per contenere tutto il testo all'interno di un oggetto. |
| Exactly | 1 | L'altezza è specificata esattamente in punti. Nota che se il testo non può entrare nell'oggetto di questa altezza, verrà troncato. |
| Auto | 2 | L'altezza crescerà automaticamente per contenere tutto il testo all'interno di un oggetto. |


## Esempi



Mostra come formattare le righe con un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Inizia una seconda riga, quindi configura la sua altezza. Il builder applicherà queste impostazioni a
// la sua riga corrente, così come a tutte le nuove righe che creerà successivamente.
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// La prima riga non è stata influenzata dalla riconfigurazione del padding e mantiene ancora i valori predefiniti.
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
