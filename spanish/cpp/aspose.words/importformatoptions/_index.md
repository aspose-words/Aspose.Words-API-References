---
title: "Aspose::Words::ImportFormatOptions clase"
linktitle: "ImportFormatOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ImportFormatOptions clase. Permite especificar varias opciones de importación para formatear la salida. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 35000
url: /es/cpp/aspose.words/importformatoptions/
---
## ImportFormatOptions class


Permite especificar varias opciones de importación para formatear la salida. Para obtener más información, visite el artículo de documentación [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class ImportFormatOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/)() const | Obtiene o establece un valor booleano que especifica si se debe ajustar automáticamente el espaciado de oraciones y palabras. El valor predeterminado es **false**. |
| [get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/)() const | Obtiene o establece un valor booleano que indica si se debe cambiar el tipo de la primera sección importada a [NewPage](../sectionstart/) de forma forzada al llamar a [AppendDocument()](../). El valor predeterminado es **true**. |
| [get_ForceCopyStyles](./get_forcecopystyles/)() const | Obtiene o establece un valor booleano que indica si se deben copiar los estilos conflictivos en modo [KeepSourceFormatting](../importformatmode/). El valor predeterminado es **false**. |
| [get_IgnoreHeaderFooter](./get_ignoreheaderfooter/)() const | Obtiene o establece un valor booleano que especifica que el formato de origen del contenido de encabezados/pies de página se ignora si se usa el modo [KeepSourceFormatting](../importformatmode/). El valor predeterminado es **true**. |
| [get_IgnoreTextBoxes](./get_ignoretextboxes/)() const | Obtiene o establece un valor booleano que especifica que el formato de origen del contenido de cuadros de texto se ignora si se usa el modo [KeepSourceFormatting](../importformatmode/). El valor predeterminado es **true**. |
| [get_KeepSourceNumbering](./get_keepsourcenumbering/)() const | Obtiene o establece un valor booleano que especifica cómo se importará la numeración cuando haya conflictos entre los documentos de origen y destino. El valor predeterminado es **false**. |
| [get_MergePastedLists](./get_mergepastedlists/)() const | Obtiene o establece un valor booleano que especifica si las listas pegadas se fusionarán con las listas circundantes. El valor predeterminado es **false**. |
| [get_ResolveThemeColors](./get_resolvethemecolors/)() const | Obtiene o establece un valor booleano que especifica si se deben resolver forzadamente los colores de tema de las formas. El valor predeterminado es **false**. |
| [get_SmartStyleBehavior](./get_smartstylebehavior/)() const | Obtiene o establece un valor booleano que especifica cómo se importarán los estilos cuando tengan nombres iguales en los documentos de origen y destino. El valor predeterminado es **false**. |
| [GetType](./gettype/)() const override |  |
| [ImportFormatOptions](./importformatoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AdjustSentenceAndWordSpacing](./set_adjustsentenceandwordspacing/)(bool) | Setter para [Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing](./get_adjustsentenceandwordspacing/). |
| [set_AppendDocumentWithNewPage](./set_appenddocumentwithnewpage/)(bool) | Setter para [Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage](./get_appenddocumentwithnewpage/). |
| [set_ForceCopyStyles](./set_forcecopystyles/)(bool) | Setter para [Aspose::Words::ImportFormatOptions::get_ForceCopyStyles](./get_forcecopystyles/). |
| [set_IgnoreHeaderFooter](./set_ignoreheaderfooter/)(bool) | Setter para [Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter](./get_ignoreheaderfooter/). |
| [set_IgnoreTextBoxes](./set_ignoretextboxes/)(bool) | Setter para [Aspose::Words::ImportFormatOptions::get_IgnoreTextBoxes](./get_ignoretextboxes/). |
| [set_KeepSourceNumbering](./set_keepsourcenumbering/)(bool) | Setter para [Aspose::Words::ImportFormatOptions::get_KeepSourceNumbering](./get_keepsourcenumbering/). |
| [set_MergePastedLists](./set_mergepastedlists/)(bool) | Setter para [Aspose::Words::ImportFormatOptions::get_MergePastedLists](./get_mergepastedlists/). |
| [set_ResolveThemeColors](./set_resolvethemecolors/)(bool) | Setter para [Aspose::Words::ImportFormatOptions::get_ResolveThemeColors](./get_resolvethemecolors/). |
| [set_SmartStyleBehavior](./set_smartstylebehavior/)(bool) | Método setter para [Aspose::Words::ImportFormatOptions::get_SmartStyleBehavior](./get_smartstylebehavior/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
