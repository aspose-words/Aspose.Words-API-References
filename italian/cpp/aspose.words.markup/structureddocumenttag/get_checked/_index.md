---
title: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_Checked"
linktitle: "get_Checked"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_Checked. Ottiene/Imposta lo stato corrente del SDT Checkbox. Il valore predefinito per questa proprietà è false in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.markup/structureddocumenttag/get_checked/
---
## StructuredDocumentTag::get_Checked method


Ottiene/Imposta lo stato corrente della casella di controllo **SDT**. Il valore predefinito per questa proprietà è **false**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_Checked()
```

## Note


L'accesso a questa proprietà funzionerà solo per i tipi SDT [Checkbox](../../sdttype/).

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
