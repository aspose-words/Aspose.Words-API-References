---
title: "Método Aspose::Words::Style::get_Name"
linktitle: "get_Name"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Style::get_Name. Obtiene o establece el nombre del estilo en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words/style/get_name/
---
## Style::get_Name method


Obtiene o establece el nombre del estilo.

```cpp
System::String Aspose::Words::Style::get_Name() const
```

## Observaciones


No puede ser una cadena vacía.

Si ya existe un estilo con ese nombre en la colección, este estilo lo sobrescribirá. Todos los nodos afectados harán referencia al nuevo estilo.

## Ejemplos



Muestra cómo acceder a la colección de estilos de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Enumere y liste todos los estilos que contiene por defecto un documento creado con Aspose.Words.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> stylesEnum = doc->get_Styles()->GetEnumerator();
    while (stylesEnum->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Style> curStyle = stylesEnum->get_Current();
        std::cout << System::String::Format(u"Style name:\t\"{0}\", of type \"{1}\"", curStyle->get_Name(), curStyle->get_Type()) << std::endl;
        std::cout << System::String::Format(u"\tSubsequent style:\t{0}", curStyle->get_NextParagraphStyleName()) << std::endl;
        std::cout << System::String::Format(u"\tIs heading:\t\t\t{0}", curStyle->get_IsHeading()) << std::endl;
        std::cout << System::String::Format(u"\tIs QuickStyle:\t\t{0}", curStyle->get_IsQuickStyle()) << std::endl;

        ASPOSE_ASSERT_EQ(doc, curStyle->get_Document());
    }
}
```


Muestra cómo clonar el estilo de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// El método AddCopy crea una copia del estilo especificado y
// genera automáticamente un nuevo nombre para el estilo, como "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Utilice la propiedad "Name" del estilo para cambiar el nombre identificador del estilo.
newStyle->set_Name(u"My Heading 1");

// Nuestro documento ahora tiene dos estilos de apariencia idéntica con nombres diferentes.
// Cambiar la configuración de uno de los estilos no afecta al otro.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```

## Ver también

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
