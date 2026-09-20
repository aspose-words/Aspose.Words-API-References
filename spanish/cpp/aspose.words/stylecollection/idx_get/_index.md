---
title: "Aspose::Words::StyleCollection::idx_get método"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::StyleCollection::idx_get método. Obtiene un estilo incorporado mediante su identificador independiente de la configuración regional en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words/stylecollection/idx_get/
---
## StyleCollection::idx_get(Aspose::Words::StyleIdentifier) method


Obtiene un estilo incorporado por su identificador independiente de la configuración regional.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(Aspose::Words::StyleIdentifier sti)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sti | Aspose::Words::StyleIdentifier | Un valor [StyleIdentifier](../../styleidentifier/) que especifica el estilo incorporado a recuperar. |
## Observaciones


Al acceder a un estilo que aún no existe, lo crea automáticamente.

## Ejemplos



Muestra cómo agregar un [Style](../../style/) a la colección de estilos de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Establezca los parámetros predeterminados para los nuevos estilos que luego podamos agregar a esta colección.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Si añadimos un estilo de "StyleType.Paragraph", la colección aplicará los valores de
// su propiedad "DefaultParagraphFormat" a la propiedad "ParagraphFormat" del estilo.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Añade un estilo y luego verifica que tiene la configuración predeterminada.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Ver también

* Class [Style](../../style/)
* Enum [StyleIdentifier](../../styleidentifier/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(const System::String\&) method


Obtiene un estilo por nombre o alias.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(const System::String &name)
```

## Observaciones


Sensible a mayúsculas y minúsculas, devuelve **null** si no se encuentra el estilo con el nombre especificado.

Si este es un nombre en inglés de un estilo incorporado que aún no existe, lo crea automáticamente.

## Ejemplos



Muestra cuándo recalcular el diseño de página del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Guardar un documento en PDF, en una imagen o imprimirlo por primera vez lo hará automáticamente
// almacenar en caché el diseño del documento dentro de sus páginas.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// Modifique el documento de alguna manera.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// En la versión actual de Aspose.Words, modificar el documento no vuelve a reconstruir automáticamente
// el diseño de página en caché. Si deseamos que el diseño en caché
// se mantenga actualizado, necesitaremos actualizarlo manualmente.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## Ver también

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## StyleCollection::idx_get(int32_t) method


Obtiene un estilo por índice.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::idx_get(int32_t index)
```


## Ejemplos



Muestra cómo agregar un [Style](../../style/) a la colección de estilos de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Establezca los parámetros predeterminados para los nuevos estilos que luego podamos agregar a esta colección.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Si añadimos un estilo de "StyleType.Paragraph", la colección aplicará los valores de
// su propiedad "DefaultParagraphFormat" a la propiedad "ParagraphFormat" del estilo.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Añade un estilo y luego verifica que tiene la configuración predeterminada.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Ver también

* Class [Style](../../style/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
