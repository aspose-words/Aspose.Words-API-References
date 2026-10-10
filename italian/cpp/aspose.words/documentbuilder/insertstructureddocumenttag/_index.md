---
title: "Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag method"
linktitle: "InsertStructuredDocumentTag"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag method. Inserisce un StructuredDocumentTag nel documento in C++."
type: docs
weight: 46500
url: /it/cpp/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder::InsertStructuredDocumentTag method


Inserisce un [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) nel documento.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType type)
```


### ReturnValue

Il nodo [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) appena inserito.

## Esempi



Mostra come inserire semplicemente un tag di documento strutturato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveTo(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(3));
// Nota, che solo i seguenti tipi di StructuredDocumentTag sono consentiti per l'inserimento:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.Date.
// Il livello di markup dello StructuredDocumentTag inserito verrà rilevato automaticamente e dipende dalla posizione in cui viene inserito.
// Lo StructuredDocumentTag aggiunto erediterà la formattazione di paragrafo e carattere dalla posizione del cursore.
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> sdtPlain = builder->InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType::PlainText);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

## Vedi anche

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Enum [SdtType](../../../aspose.words.markup/sdttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
