---
title: "Aspose::Words::Tables::PreferredWidthType enum"
linktitle: "PreferredWidthType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::PreferredWidthType enum. Specifica l'unità di misura per la larghezza preferita di una tabella o di una cella in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enum


Specifica l'unità di misura per la larghezza preferita di una tabella o di una cella.

```cpp
enum class PreferredWidthType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | 1 | La larghezza preferita non è specificata. La larghezza effettiva della tabella o della cella è specificata utilizzando la larghezza esplicita oppure verrà determinata automaticamente dall'algoritmo di layout della tabella quando la tabella viene visualizzata, a seconda dell'impostazione di adattamento automatico della tabella. |
| Percentuale | 2 | Misura la larghezza corrente dell'elemento usando una percentuale specificata. |
| Punti | 3 | Misura la larghezza corrente dell'elemento usando un numero specificato di punti (1/72 di pollice). |


## Esempi



Mostra come verificare il tipo e il valore della larghezza preferita di una cella di tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Vedi anche

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
