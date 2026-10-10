---
title: "Aspose::Words::MailMerging::MailMergeCleanupOptions enum"
linktitle: "MailMergeCleanupOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::MailMerging::MailMergeCleanupOptions enum. Specifica le opzioni che determinano quali elementi vengono rimossi durante l'unione della posta in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enum


Specifica le opzioni che determinano quali elementi vengono rimossi durante l'unione della posta.

```cpp
enum class MailMergeCleanupOptions
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Specifica un valore predefinito. |
| RemoveEmptyParagraphs | 1 | Specifica se i paragrafi che contenevano campi di unione senza dati devono essere rimossi dal documento. Quando questa opzione è impostata, vengono rimossi anche i paragrafi che contengono campi di inizio e fine regione di unione che sono altrimenti vuoti. |
| RemoveUnusedRegions | 2 | Specifica se le regioni di unione della posta non utilizzate devono essere rimosse dal documento. |
| RemoveUnusedFields | 4 | Specifica se i campi di unione non utilizzati devono essere rimossi dal documento. |
| RemoveContainingFields | 8 | Specifica se i campi che contengono campi di unione (ad esempio, IF) devono essere rimossi dal documento se i campi di unione nidificati vengono rimossi. |
| RemoveStaticFields | 16 | Specifica se i campi statici devono essere rimossi dal documento. I campi statici sono campi i cui risultati rimangono invariati a seguito di qualsiasi modifica del documento. [Fields](../../aspose.words.fields/), che non memorizzano i loro risultati in un documento e sono calcolati al volo (come [FieldListNum](../../aspose.words.fields/fieldtype/), [FieldSymbol](../../aspose.words.fields/fieldtype/), ecc.) non sono considerati statici. |
| RemoveEmptyTableRows | 32 | Specifica se le righe vuote che contengono regioni di unione della posta devono essere rimosse dal documento. |
| RemoveEmptyTables | 64 | Specifica se rimuovere dal documento le tabelle che contengono regioni di unione della posta che sono state rimosse usando l'opzione [RemoveUnusedRegions](./) o [RemoveEmptyTableRows](./). |

## Vedi anche

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
