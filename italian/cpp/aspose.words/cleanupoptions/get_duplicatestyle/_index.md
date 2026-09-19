---
title: "Metodo Aspose::Words::CleanupOptions::get_DuplicateStyle"
linktitle: "get_DuplicateStyle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::CleanupOptions::get_DuplicateStyle. Ottiene/imposta un flag che indica se gli stili duplicati devono essere rimossi dal documento. Il valore predefinito è false in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/cleanupoptions/get_duplicatestyle/
---
## CleanupOptions::get_DuplicateStyle method


Ottiene/imposta un flag che indica se gli stili duplicati devono essere rimossi dal documento. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::CleanupOptions::get_DuplicateStyle() const
```


## Esempi



Mostra come rimuovere gli stili duplicati dal documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aggiungi due stili al documento con proprietà identiche,
// ma nomi diversi. Il secondo stile è considerato un duplicato del primo.
System::SharedPtr<Aspose::Words::Style> myStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

System::SharedPtr<Aspose::Words::Style> duplicateStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle2");
duplicateStyle->get_Font()->set_Size(14);
duplicateStyle->get_Font()->set_Name(u"Courier New");
duplicateStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// Applica entrambi gli stili a paragrafi diversi all'interno del documento.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

builder->get_ParagraphFormat()->set_StyleName(duplicateStyle->get_Name());
builder->Writeln(u"Hello again!");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(duplicateStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());

// Configura un oggetto CleanOptions, quindi chiama il metodo Cleanup per sostituire tutti gli stili duplicati
// con l'originale e rimuovi i duplicati dal documento.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_DuplicateStyle(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(5, doc->get_Styles()->get_Count());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## Vedi anche

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
