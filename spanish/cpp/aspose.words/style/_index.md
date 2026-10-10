---
title: "Aspose::Words::Style clase"
linktitle: "Estilo"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Style clase. Representa un estilo incorporado o definido por el usuario. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 64000
url: /es/cpp/aspose.words/style/
---
## Style class


Representa un estilo único incorporado o definido por el usuario. Para obtener más información, visite el artículo de documentación [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class Style : public Aspose::Words::IParaAttrSource,
              public Aspose::Words::IRunAttrSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Compara con el estilo especificado. Los Istds de estilos se comparan solo para estilos incorporados. Los valores predeterminados de los estilos no se incluyen en la comparación. El estilo base, el estilo enlazado y el estilo del siguiente párrafo se comparan recursivamente. |
| [get_Aliases](./get_aliases/)() | Obtiene todos los alias de este estilo. Si el estilo no tiene alias, se devuelve una matriz vacía de cadenas. |
| [get_AutomaticallyUpdate](./get_automaticallyupdate/)() const | Especifica si este estilo se redefine automáticamente según el valor apropiado. |
| [get_BaseStyleName](./get_basestylename/)() | Obtiene/establece el nombre del estilo del que se basa este estilo. |
| [get_BuiltIn](./get_builtin/)() | Verdadero si este estilo es uno de los estilos incorporados en MS Word. |
| [get_Document](./get_document/)() | Obtiene el documento propietario. |
| [get_Font](./get_font/)() | Obtiene el formato de caracteres del estilo. |
| [get_IsHeading](./get_isheading/)() | Verdadero cuando el estilo es uno de los estilos de encabezado incorporados. |
| [get_IsQuickStyle](./get_isquickstyle/)() const | Especifica si este estilo se muestra en la galería rápida de [Style](./) dentro de la interfaz de MS Word. |
| [get_LinkedStyleName](./get_linkedstylename/)() | Obtiene/establece el nombre del [Style](./) vinculado a este. Devuelve una cadena vacía si no hay estilos vinculados. |
| [get_List](./get_list/)() | Obtiene la lista que define el formato de este estilo de lista. |
| [get_ListFormat](./get_listformat/)() | Proporciona acceso a las propiedades de formato de lista de un estilo de párrafo. |
| [get_Locked](./get_locked/)() const | Especifica si este estilo está bloqueado. |
| [get_Name](./get_name/)() const | Obtiene o establece el nombre del estilo. |
| [get_NextParagraphStyleName](./get_nextparagraphstylename/)() | Obtiene/establece el nombre del estilo que se aplicará automáticamente a un nuevo párrafo insertado después de un párrafo formateado con el estilo especificado. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Obtiene el formato de párrafo del estilo. |
| [get_Priority](./get_priority/)() const | Obtiene/establece el valor entero que representa la prioridad para ordenar los estilos en el panel de tareas de Estilos. |
| [get_SemiHidden](./get_semihidden/)() const | Obtiene/establece si el estilo se oculta de la galería de Estilos y del panel de tareas de Estilos. |
| [get_StyleIdentifier](./get_styleidentifier/)() const | Obtiene el identificador de estilo independiente de la configuración regional para un estilo incorporado. |
| [get_Styles](./get_styles/)() const | Obtiene la colección de estilos a la que pertenece este estilo. |
| [get_Type](./get_type/)() const | Obtiene el tipo de estilo (párrafo o carácter). |
| [get_UnhideWhenUsed](./get_unhidewhenused/)() const | Obtiene/establece si el estilo usado en el documento actual se muestra en la galería de Estilos y en el panel de tareas de Estilos. Verdadero cuando el estilo usado debe mostrarse en la galería de Estilos. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Elimina el estilo especificado del documento. |
| [set_AutomaticallyUpdate](./set_automaticallyupdate/)(bool) | Método set para [Aspose::Words::Style::get_AutomaticallyUpdate](./get_automaticallyupdate/). |
| [set_BaseStyleName](./set_basestylename/)(const System::String\&) | Método set para [Aspose::Words::Style::get_BaseStyleName](./get_basestylename/). |
| [set_IsQuickStyle](./set_isquickstyle/)(bool) | Método set para [Aspose::Words::Style::get_IsQuickStyle](./get_isquickstyle/). |
| [set_LinkedStyleName](./set_linkedstylename/)(const System::String\&) | Método set para [Aspose::Words::Style::get_LinkedStyleName](./get_linkedstylename/). |
| [set_Locked](./set_locked/)(bool) | Método set para [Aspose::Words::Style::get_Locked](./get_locked/). |
| [set_Name](./set_name/)(const System::String\&) | Método set para [Aspose::Words::Style::get_Name](./get_name/). |
| [set_NextParagraphStyleName](./set_nextparagraphstylename/)(const System::String\&) | Método set para [Aspose::Words::Style::get_NextParagraphStyleName](./get_nextparagraphstylename/). |
| [set_Priority](./set_priority/)(int32_t) | Método set para [Aspose::Words::Style::get_Priority](./get_priority/). |
| [set_SemiHidden](./set_semihidden/)(bool) | Método set para [Aspose::Words::Style::get_SemiHidden](./get_semihidden/). |
| [set_UnhideWhenUsed](./set_unhidewhenused/)(bool) | Método set para [Aspose::Words::Style::get_UnhideWhenUsed](./get_unhidewhenused/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo crear y aplicar un estilo personalizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Redefinir el estilo automáticamente.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aplica uno de los estilos del documento al párrafo que el generador de documentos está creando.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Elimina nuestro estilo personalizado de la colección de estilos del documento.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Cualquier texto que utilizó un estilo eliminado vuelve al formato predeterminado.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```


Muestra cómo crear y usar un estilo de párrafo con formato de lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un estilo de párrafo personalizado.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Crea una lista y asegura que los párrafos que usan este estilo utilicen esta lista.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Aplica el estilo de párrafo al párrafo actual del generador de documentos y luego agrega algo de texto.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Cambie el estilo del document builder a uno que no tenga formato de lista y escriba otro párrafo.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
