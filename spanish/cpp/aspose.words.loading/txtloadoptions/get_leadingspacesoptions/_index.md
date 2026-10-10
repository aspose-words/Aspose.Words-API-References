---
title: "Método Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions"
linktitle: "get_LeadingSpacesOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions método. Obtiene o establece la opción preferida de manejo de espacios iniciales. El valor predeterminado es ConvertToIndent en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.loading/txtloadoptions/get_leadingspacesoptions/
---
## TxtLoadOptions::get_LeadingSpacesOptions method


Obtiene o establece la opción preferida de manejo de espacios iniciales. El valor predeterminado es [ConvertToIndent](../../txtleadingspacesoptions/).

```cpp
Aspose::Words::Loading::TxtLeadingSpacesOptions Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions() const
```


## Ejemplos



Muestra cómo recortar espacios en blanco al cargar documentos de texto sin formato.
```cpp
System::String textDoc = System::String(u"      Line 1 \n") + u"    Line 2   \n" + u" Line 3       ";

// Cree un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento
// para modificar cómo cargamos un documento de texto plano.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Establezca la propiedad \"LeadingSpacesOptions\" a \"TxtLeadingSpacesOptions.Preserve\"
// para preservar todos los caracteres de espacio en blanco al inicio de cada línea.
// Establezca la propiedad "LeadingSpacesOptions" a "TxtLeadingSpacesOptions.ConvertToIndent"
// para eliminar todos los caracteres de espacio en blanco al inicio de cada línea,
// y luego aplique una sangría izquierda en la primera línea del párrafo para simular el efecto de los espacios en blanco.
// Establezca la propiedad "LeadingSpacesOptions" a "TxtLeadingSpacesOptions.Trim"
// para eliminar todos los caracteres de espacio en blanco al inicio de cada línea.
loadOptions->set_LeadingSpacesOptions(txtLeadingSpacesOptions);

// Establezca la propiedad "TrailingSpacesOptions" a "TxtTrailingSpacesOptions.Preserve"
// para preservar todos los caracteres de espacio en blanco al final de cada línea.
// Establezca la propiedad "TrailingSpacesOptions" a "TxtTrailingSpacesOptions.Trim" para
// eliminar todos los caracteres de espacio en blanco al final de cada línea.
loadOptions->set_TrailingSpacesOptions(txtTrailingSpacesOptions);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

switch (txtLeadingSpacesOptions)
{
    case Aspose::Words::Loading::TxtLeadingSpacesOptions::ConvertToIndent:
        ASPOSE_ASSERT_EQ(37.8, paragraphs->idx_get(0)->get_ParagraphFormat()->get_FirstLineIndent());
        ASPOSE_ASSERT_EQ(25.2, paragraphs->idx_get(1)->get_ParagraphFormat()->get_FirstLineIndent());
        ASPOSE_ASSERT_EQ(6.3, paragraphs->idx_get(2)->get_ParagraphFormat()->get_FirstLineIndent());
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u"Line 3"));
        break;

    case Aspose::Words::Loading::TxtLeadingSpacesOptions::Preserve:
        ASSERT_TRUE(paragraphs->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
        {
            return (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_ParagraphFormat()->get_FirstLineIndent() == 0.0;
        }))));
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"      Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"    Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u" Line 3"));
        break;

    case Aspose::Words::Loading::TxtLeadingSpacesOptions::Trim:
        ASSERT_TRUE(paragraphs->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
        {
            return (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_ParagraphFormat()->get_FirstLineIndent() == 0.0;
        }))));
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u"Line 3"));
        break;

}

switch (txtTrailingSpacesOptions)
{
    case Aspose::Words::Loading::TxtTrailingSpacesOptions::Preserve:
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().EndsWith(u"Line 1 \r"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().EndsWith(u"Line 2   \r"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().EndsWith(u"Line 3       \f"));
        break;

    case Aspose::Words::Loading::TxtTrailingSpacesOptions::Trim:
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().EndsWith(u"Line 1\r"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().EndsWith(u"Line 2\r"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().EndsWith(u"Line 3\f"));
        break;

}
```

## Ver también

* Enum [TxtLeadingSpacesOptions](../../txtleadingspacesoptions/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
