---
title: "Aspose::Words::Markup::StructuredDocumentTag::SetCheckedSymbol method"
linktitle: "SetCheckedSymbol"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTag::SetCheckedSymbol. Imposta il simbolo utilizzato per rappresentare lo stato selezionato di un controllo di contenuto casella di controllo in C++."
type: docs
weight: 58000
url: /it/cpp/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag::SetCheckedSymbol method


Imposta il simbolo usato per rappresentare lo stato selezionato di un controllo casella di controllo.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::SetCheckedSymbol(int32_t characterCode, const System::String &fontName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| characterCode | int32_t | Il codice carattere per il simbolo specificato. |
| fontName | const System::String\& | Il nome del font che contiene il simbolo. |
## Note


L'accesso a questo metodo funzionerà solo per i tipi SDT [Checkbox](../../sdttype/).

Per tutti gli altri tipi SDT si verificherà un'eccezione.

## Esempi



Mostra come creare un tag di documento strutturato sotto forma di casella di controllo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto sdtCheckBox = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
sdtCheckBox->set_Checked(true);

// Possiamo impostare i simboli usati per rappresentare lo stato selezionato/non selezionato di un controllo contenuto di casella di controllo.
sdtCheckBox->SetCheckedSymbol(0x00A9, u"Times New Roman");
sdtCheckBox->SetUncheckedSymbol(0x00AE, u"Times New Roman");

builder->InsertNode(sdtCheckBox);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CheckBox.docx");
```

## Vedi anche

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
