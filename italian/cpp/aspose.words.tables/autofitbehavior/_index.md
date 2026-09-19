---
title: "Aspose::Words::Tables::AutoFitBehavior enum"
linktitle: "AutoFitBehavior"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::AutoFitBehavior enum. Determina come Aspose.Words ridimensiona la tabella quando invochi il metodo AutoFit() in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enum


Determina come Aspose.Words ridimensiona la tabella quando invochi il metodo [AutoFit()](../table/autofit/).

```cpp
enum class AutoFitBehavior
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| AutoFitToContents | 0 | Aspose.Words abilita l'opzione AutoFit, rimuove la larghezza preferita dalla tabella e da tutte le celle e poi aggiorna il layout della tabella. Nella tabella risultante, le larghezze delle celle vengono aggiornate per adattarsi al contenuto della tabella. È probabile che la tabella si riduca. |
| AutoFitToWindow | 1 | Quando utilizzi questo valore, Aspose.Words abilita l'opzione AutoFit, imposta la larghezza preferita della tabella al 100%, rimuove le larghezze preferite da tutte le celle e poi aggiorna il layout della tabella. Di conseguenza, la tabella occupa tutta la larghezza disponibile e le larghezze delle celle vengono aggiornate per adattarsi al contenuto della tabella. |
| FixedColumnWidths | 2 | Aspose.Words disabilita l'opzione AutoFit e rimuove la larghezza preferita dalla tabella. Le larghezze delle celle rimangono così come sono specificate dalle loro proprietà [Width](../cellformat/get_width/). |


## Esempi



Mostra come creare una nuova tabella applicando uno stile.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Dobbiamo inserire almeno una riga prima di impostare qualsiasi formattazione della tabella.
builder->InsertCell();

// Imposta lo stile della tabella da utilizzare in base all'identificatore dello stile.
// Nota che non tutti gli stili di tabella sono disponibili quando si salva nel formato .doc.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// Applica parzialmente lo stile alle caratteristiche della tabella in base a predicati, quindi costruisci la tabella.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
