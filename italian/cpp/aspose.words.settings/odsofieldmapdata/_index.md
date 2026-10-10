---
title: "Aspose::Words::Settings::OdsoFieldMapData classe"
linktitle: "OdsoFieldMapData"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Settings::OdsoFieldMapData class. Specifica come una colonna nella fonte dati esterna deve essere mappata ai campi di unione predefiniti nel documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class


Specifica come una colonna nella fonte dati esterna deve essere mappata ai campi di unione predefiniti all'interno del documento. Per saperne di più, visita l'articolo di documentazione [Unione di posta e reportistica](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoFieldMapData : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clone](./clone/)() | Restituisce una copia profonda di questo oggetto. |
| [get_Column](./get_column/)() const | Specifica l'indice basato su zero della colonna all'interno di una fonte dati esterna che deve essere mappata al nome locale di un campo MERGEFIELD specifico. Il valore predefinito è 0. |
| [get_MappedName](./get_mappedname/)() const | Specifica il nome del campo di unione predefinito che deve essere mappato al numero di colonna specificato dalla proprietà [Column](./get_column/) in questa mappatura di campo. Il valore predefinito è una stringa vuota. |
| [get_Name](./get_name/)() const | Specifica il nome della colonna all'interno di una fonte dati esterna per la colonna il cui indice è specificato dalla proprietà [Column](./get_column/). Il valore predefinito è una stringa vuota. |
| [get_Type](./get_type/)() const | Specifica se un determinato campo di stampa unione è stato mappato a una colonna nella fonte dati esterna fornita o meno. Il valore predefinito è [Default](../odsofieldmappingtype/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoFieldMapData](./odsofieldmapdata/)() |  |
| [set_Column](./set_column/)(int32_t) | Specifica l'indice basato su zero della colonna all'interno di una fonte dati esterna che deve essere mappata al nome locale di un campo MERGEFIELD specifico. Il valore predefinito è 0. |
| [set_MappedName](./set_mappedname/)(const System::String\&) | Specifica il nome del campo di unione predefinito che deve essere mappato al numero di colonna specificato dalla proprietà [Column](./get_column/) in questa mappatura di campo. Il valore predefinito è una stringa vuota. |
| [set_Name](./set_name/)(const System::String\&) | Specifica il nome della colonna all'interno di una fonte dati esterna per la colonna il cui indice è specificato dalla proprietà [Column](./get_column/). Il valore predefinito è una stringa vuota. |
| [set_Type](./set_type/)(Aspose::Words::Settings::OdsoFieldMappingType) | Specifica se un determinato campo di stampa unione è stato mappato a una colonna nella fonte dati esterna fornita o meno. Il valore predefinito è [Default](../odsofieldmappingtype/). |
| static [Type](./type/)() |  |
## Note


Microsoft Word fornisce alcuni nomi di campi di unione predefiniti che consente di inserire in un documento come MERGEFIELD o di utilizzare nei campi ADDRESSBLOCK o GREETINGLINE. Le informazioni specificate in [OdsoFieldMapData](./) consentono di mappare una colonna nella fonte dati esterna a un singolo campo di unione predefinito.

## Vedi anche

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
