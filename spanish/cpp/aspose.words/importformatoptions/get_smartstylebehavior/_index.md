---
title: "Método Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior"
linktitle: "get_SmartStyleBehavior"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior. Obtiene o establece un valor booleano que especifica cómo se importarán los estilos cuando tengan nombres iguales en los documentos de origen y destino. El valor predeterminado es false en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words/importformatoptions/get_smartstylebehavior/
---
## ImportFormatOptions::get_SmartStyleBehavior method


Obtiene o establece un valor booleano que especifica cómo se importarán los estilos cuando tengan nombres iguales en los documentos de origen y destino. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior() const
```

## Observaciones


Cuando esta opción está **habilitada**, el estilo de origen se expandirá en atributos directos dentro de un documento de destino, si se utiliza el modo de importación [KeepSourceFormatting](../../importformatmode/).

Cuando esta opción está **deshabilitada**, el estilo de origen se expandirá solo si está numerado. Los atributos de destino existentes no se sobrescribirán, incluidas las listas.

## Ejemplos



Muestra cómo resolver estilos duplicados al insertar documentos.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);

System::SharedPtr<Aspose::Words::Style> myStyle = builder->get_Document()->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
myStyle->get_Font()->set_Size(14);
myStyle->get_Font()->set_Name(u"Courier New");
myStyle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

builder->get_ParagraphFormat()->set_StyleName(myStyle->get_Name());
builder->Writeln(u"Hello world!");

// Clona el documento y edita el estilo "MyStyle" del clon, de modo que tenga un color diferente al del original.
// Si insertamos el clon en el documento original, los dos estilos con el mismo nombre causarán un conflicto.
System::SharedPtr<Aspose::Words::Document> srcDoc = dstDoc->Clone();
srcDoc->get_Styles()->idx_get(u"MyStyle")->get_Font()->set_Color(System::Drawing::Color::get_Red());

// Cuando habilitamos SmartStyleBehavior y usamos el modo de formato de importación KeepSourceFormatting,
// Aspose.Words resolverá los conflictos de estilo convirtiendo los estilos del documento fuente.
// con los mismos nombres que los estilos de destino en atributos de párrafo directos.
auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_SmartStyleBehavior(true);

builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.SmartStyleBehavior.docx");
```

## Ver también

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
