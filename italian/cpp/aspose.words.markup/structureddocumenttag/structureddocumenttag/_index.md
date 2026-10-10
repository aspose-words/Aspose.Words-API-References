---
title: "Costruttore Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag"
linktitle: "StructuredDocumentTag"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag. Inizializza una nuova istanza della classe Structured document tag in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag::StructuredDocumentTag constructor


Inizializza una nuova istanza della classe **Structured document tag**.

```cpp
Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Markup::SdtType type, Aspose::Words::Markup::MarkupLevel level)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento proprietario. |
| tipo | Aspose::Words::Markup::SdtType | Tipo di nodo SDT. |
| livello | Aspose::Words::Markup::MarkupLevel | Livello del nodo SDT all'interno del documento. |
## Note


È possibile creare i seguenti tipi di SDT:

* [Checkbox](../../sdttype/)
* [DropDownList](../../sdttype/)
* [ComboBox](../../sdttype/)
* [Date](../../sdttype/)
* [BuildingBlockGallery](../../sdttype/)
* [Group](../../sdttype/)
* [Picture](../../sdttype/)
* [RichText](../../sdttype/)
* [PlainText](../../sdttype/)



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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [SdtType](../../sdttype/)
* Enum [MarkupLevel](../../markuplevel/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
