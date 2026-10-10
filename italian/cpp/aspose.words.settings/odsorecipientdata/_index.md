---
title: "Classe Aspose::Words::Settings::OdsoRecipientData"
linktitle: "OdsoRecipientData"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Settings::OdsoRecipientData. Rappresenta le informazioni su un singolo record all'interno di una fonte dati esterna che deve essere escluso dall'unione della posta. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class


Rappresenta le informazioni su un singolo record in una fonte dati esterna che deve essere escluso dall'unione di posta. Per saperne di più, visita l'articolo di documentazione [Unione di posta e reportistica](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoRecipientData : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clone](./clone/)() | Restituisce una copia profonda di questo oggetto. |
| [get_Active](./get_active/)() const | Specifica se il record dalla fonte dati deve essere importato in un documento quando viene eseguita l'unione della posta. Il valore predefinito è **true**. |
| [get_Column](./get_column/)() const | Specifica la colonna nella fonte dati che contiene dati univoci per il record corrente. Il valore predefinito è 0. |
| [get_Hash](./get_hash/)() const | Rappresenta il codice hash per questo record. Talvolta Microsoft Word utilizza [Hash](./get_hash/) di un intero record invece di un valore [UniqueTag](./get_uniquetag/). Il valore predefinito è 0. |
| [get_UniqueTag](./get_uniquetag/)() const | Specifica il contenuto di un determinato record nella colonna contenente dati univoci. Il valore predefinito è **null**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoRecipientData](./odsorecipientdata/)() |  |
| [set_Active](./set_active/)(bool) | Specifica se il record dalla fonte dati deve essere importato in un documento quando viene eseguita l'unione della posta. Il valore predefinito è **true**. |
| [set_Column](./set_column/)(int32_t) | Specifica la colonna nella fonte dati che contiene dati univoci per il record corrente. Il valore predefinito è 0. |
| [set_Hash](./set_hash/)(int32_t) | Rappresenta il codice hash per questo record. Talvolta Microsoft Word utilizza [Hash](./get_hash/) di un intero record invece di un valore [UniqueTag](./get_uniquetag/). Il valore predefinito è 0. |
| [set_UniqueTag](./set_uniquetag/)(const System::ArrayPtr\<uint8_t\>\&) | Specifica il contenuto di un determinato record nella colonna contenente dati univoci. Il valore predefinito è **null**. |
| static [Type](./type/)() |  |
## Note


Se un record deve essere unito a un documento unito, non è necessaria alcuna informazione su quel record. Tuttavia, se un determinato record non deve essere unito a un documento unito, il valore della chiave univoca per quel record deve essere memorizzato nella proprietà [UniqueTag](./get_uniquetag/) di questo oggetto per indicare questa esclusione.
## Vedi anche

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
