---
title: "Método Aspose::Words::ImportFormatOptions::get_ResolveThemeColors"
linktitle: "get_ResolveThemeColors"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::ImportFormatOptions::get_ResolveThemeColors. Obtiene o establece un valor booleano que especifica si se deben resolver forzadamente los colores de tema de las formas. El valor predeterminado es false en C++."
type: docs
weight: 8500
url: /es/cpp/aspose.words/importformatoptions/get_resolvethemecolors/
---
## ImportFormatOptions::get_ResolveThemeColors method


Obtiene o establece un valor booleano que especifica si se deben resolver forzadamente los colores de tema de las formas. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ResolveThemeColors() const
```

## Observaciones


Tenga en cuenta que esta opción solo es relevante para el modo [KeepSourceFormatting](../../importformatmode/).

Normalmente, Aspose.Words no resuelve los colores de tema de origen al importar estilos que pueden preservarse sin expandir los atributos de formato en directos. Sin embargo, en este caso los colores reales de las formas importadas pueden diferir de los que tenían en el documento original. La razón es que los colores de tema difieren entre los documentos de origen y destino. Establecer esta opción a **true** obliga a resolver los colores de tema de las formas de origen y, por lo tanto, a preservar el color real de las formas que tienen en el documento de origen.

## Ejemplos



Muestra cómo importar un nodo resolviendo los colores de tema origen de las formas.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Mueva al pie de página principal e inserte una forma que use los colores del tema.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Importe el pie de página de origen al documento de destino con los colores del tema resueltos,
// para que la forma preserve su color real del documento de origen.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## Ver también

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
