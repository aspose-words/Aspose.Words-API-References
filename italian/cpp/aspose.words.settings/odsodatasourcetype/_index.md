---
title: "Aspose::Words::Settings::OdsoDataSourceType enum"
linktitle: "OdsoDataSourceType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Settings::OdsoDataSourceType enum. Specifica il tipo di origine dati esterna a cui connettersi come parte delle informazioni di connessione ODSO in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enum


Specifica il tipo della fonte dati esterna a cui connettersi come parte delle informazioni di connessione ODSO.

```cpp
enum class OdsoDataSourceType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Testo | 0 | Specifica che un determinato documento è stato collegato a un file di testo. Possibilmente wdMergeSubTypeOther. |
| Database | 1 | Specifica che un determinato documento è stato collegato a un database. Possibilmente wdMergeSubTypeAccess. |
| Rubrica | 2 | Specifica che un documento dato è stato collegato a una rubrica di contatti. Possibilmente wdMergeSubTypeOAL. |
| Documento1 | 3 | Specifica che un documento dato è stato collegato a un altro formato di documento supportato dall'applicazione produttrice. Possibilmente wdMergeSubTypeOLEDBWord. |
| Documento2 | 4 | Specifica che un documento dato è stato collegato a un altro formato di documento supportato dall'applicazione produttrice. Possibilmente wdMergeSubTypeWorks. |
| Native | 5 | Specifica che un documento dato è stato collegato a un altro formato di documento nativo dell'applicazione produttrice. Possibilmente wdMergeSubTypeOLEDBText. |
| Email | 6 | Specifica che un documento dato è stato collegato a un'applicazione di posta elettronica. Possibilmente wdMergeSubTypeOutlook. |
| None | 7 | Il tipo della fonte dati esterna non è specificato. Possibilmente wdMergeSubTypeWord. |
| Legacy | 8 | Specifica che un documento dato è stato collegato a un formato di documento legacy supportato dall'applicazione produttrice Possibilmente wdMergeSubTypeWord2000. |
| Master | 9 | Specifica che un documento dato è stato collegato a una fonte dati che aggrega altre fonti dati. |
| Default | n/a | Uguale a [None](./). |

## Note


La specifica OOXML è molto vaga per questa enumerazione. Credo possa corrispondere all'enumerazione WdMergeSubType [http://msdn.microsoft.com/en-us/library/bb237801.aspx](http://msdn.microsoft.com/en-us/library/bb237801.aspx).

## Vedi anche

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
