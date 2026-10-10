---
title: "Aspose::Words::StyleCollection clase"
linktitle: "StyleCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::StyleCollection clase. Una colección de objetos Style que representan tanto los estilos incorporados como los definidos por el usuario en un documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 65000
url: /es/cpp/aspose.words/stylecollection/
---
## StyleCollection class


Una colección de objetos [Style](../style/) que representan tanto los estilos incorporados como los definidos por el usuario en un documento. Para obtener más información, visite el artículo de documentación [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class StyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Style>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(Aspose::Words::StyleType, const System::String\&) | Crea un nuevo estilo definido por el usuario y lo agrega a la colección. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Copia un estilo en esta colección. |
| [ClearQuickStyleGallery](./clearquickstylegallery/)() | Elimina todos los estilos del panel rápido de la Galería [Style](../style/). |
| [get_Count](./get_count/)() | Obtiene el número de estilos en la colección. |
| [get_DefaultFont](./get_defaultfont/)() | Obtiene el formato de texto predeterminado del documento. |
| [get_DefaultParagraphFormat](./get_defaultparagraphformat/)() | Obtiene el formato de párrafo predeterminado del documento. |
| [get_Document](./get_document/)() const | Obtiene el documento propietario. |
| [GetEnumerator](./getenumerator/)() override | Obtiene un objeto enumerador que enumerará los estilos en orden alfabético de sus nombres. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtiene un estilo por nombre o alias. |
| [idx_get](./idx_get/)(Aspose::Words::StyleIdentifier) | Obtiene un estilo incorporado por su identificador independiente de la configuración regional. |
| [idx_get](./idx_get/)(int32_t) | Obtiene un estilo por índice. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Ejemplos



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
