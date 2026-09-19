---
title: "Metodo Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate"
linktitle: "get_IsBidiTextSupportedOnUpdate"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate. Ottiene o imposta il valore che indica se il testo bidirezionale è pienamente supportato durante l'aggiornamento del campo o meno in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/
---
## FieldOptions::get_IsBidiTextSupportedOnUpdate method


Ottiene o imposta il valore che indica se il testo bidirezionale è completamente supportato durante l'aggiornamento del campo o meno.

```cpp
bool Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate() const
```

## Note


Quando questa proprietà è impostata su **true**, vengono eseguiti passaggi aggiuntivi per produrre un risultato di campo compatibile con le lingue da destra a sinistra (ad es. arabo o ebraico) durante il suo aggiornamento.

Quando questa proprietà è impostata su **false** e si utilizza una lingua da destra a sinistra, la correttezza del risultato del campo dopo l'aggiornamento non è garantita.

Il valore predefinito è **false**.

## Esempi



Mostra come utilizzare [FieldOptions](../) per garantire che l'aggiornamento del campo supporti pienamente il testo bidirezionale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Assicurati che qualsiasi operazione sul campo che coinvolga testo da destra a sinistra venga eseguita come previsto.
doc->get_FieldOptions()->set_IsBidiTextSupportedOnUpdate(true);

// Utilizza un document builder per inserire un campo che contiene il testo da destra a sinistra.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"עֶשְׂרִים", u"שְׁלוֹשִׁים", u"אַרְבָּעִים", u"חֲמִשִּׁים", u"שִׁשִּׁים"}), 0);
comboBox->set_CalculateOnExit(true);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.Bidi.docx");
```

## Vedi anche

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
