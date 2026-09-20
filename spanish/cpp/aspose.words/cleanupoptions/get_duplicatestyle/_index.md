---
title: "Método Aspose::Words::CleanupOptions::get_DuplicateStyle"
linktitle: "get_DuplicateStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::CleanupOptions::get_DuplicateStyle. Obtiene/establece una bandera que indica si los estilos duplicados deben eliminarse del documento. El valor predeterminado es false en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/cleanupoptions/get_duplicatestyle/
---
## CleanupOptions::get_DuplicateStyle method


Obtiene/establece una bandera que indica si los estilos duplicados deben eliminarse del documento. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::CleanupOptions::get_DuplicateStyle() const
```


## Ejemplos



Muestra cómo eliminar estilos duplicados del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Agregue dos estilos al documento con propiedades idénticas,
// pero con nombres diferentes. El segundo estilo se considera un duplicado del primero.
System::SharedPtr<Aspose::Words::Style> myStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

System::SharedPtr<Aspose::Words::Style> duplicateStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle2");
duplicateStyle->get_Font()->set_Size(14);
duplicateStyle->get_Font()->set_Name(u"Courier New");
duplicateStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

ASSERT_EQ(6, doc->get_Styles()->get_Count());

// Aplique ambos estilos a diferentes párrafos dentro del documento.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

builder->get_ParagraphFormat()->set_StyleName(duplicateStyle->get_Name());
builder->Writeln(u"Hello again!");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(duplicateStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());

// Configure un objeto CleanOptions, luego llame al método Cleanup para sustituir todos los estilos duplicados
// con el original y elimine los duplicados del documento.
auto cleanupOptions = System::MakeObject<Aspose::Words::CleanupOptions>();
cleanupOptions->set_DuplicateStyle(true);

doc->Cleanup(cleanupOptions);

ASSERT_EQ(5, doc->get_Styles()->get_Count());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Style());
ASPOSE_ASSERT_EQ(myStyle, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## Ver también

* Class [CleanupOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
