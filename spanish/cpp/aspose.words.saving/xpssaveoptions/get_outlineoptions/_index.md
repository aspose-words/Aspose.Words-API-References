---
title: "Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions método"
linktitle: "get_OutlineOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions método. Permite especificar opciones de esquema en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/xpssaveoptions/get_outlineoptions/
---
## XpsSaveOptions::get_OutlineOptions method


Permite especificar opciones de contorno.

```cpp
System::SharedPtr<Aspose::Words::Saving::OutlineOptions> Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions() const
```

## Observaciones


Tenga en cuenta que la opción [ExpandedOutlineLevels](../../outlineoptions/get_expandedoutlinelevels/) no funcionará al guardar en XPS.

## Ejemplos



Muestra cómo limitar el nivel de los encabezados que aparecerán en el esquema de un documento XPS guardado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte encabezados que puedan servir como entradas del índice (TOC) de los niveles 1, 2 y luego 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// Cree un objeto "XpsSaveOptions" que podamos pasar al método "Save" del documento
// para modificar cómo ese método convierte el documento a .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// El documento XPS de salida contendrá un esquema, una tabla de contenidos que enumera los encabezados en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema nos llevará a la ubicación de su encabezado correspondiente.
// Establezca la propiedad "HeadingsOutlineLevels" en "2" para excluir todos los encabezados cuyo nivel sea superior a 2 del esquema.
// Los dos últimos encabezados que insertamos arriba no aparecerán.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## Ver también

* Class [OutlineOptions](../../outlineoptions/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
