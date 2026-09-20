---
title: "Clase Aspose::Words::Document"
linktitle: "Documento"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Document. Representa un documento Word. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 20000
url: /es/cpp/aspose.words/document/
---
## Document class


Representa un documento Word. Para obtener más información, visite el artículo de documentación [Working with Document](https://docs.aspose.com/words/cpp/working-with-document/).

```cpp
class Document : public Aspose::Words::DocumentBase,
                 public Aspose::Words::ISectionAttrSource,
                 public Aspose::Words::IWatermarkProvider
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante. |
| [AcceptAllRevisions](./acceptallrevisions/)() | Acepta todos los cambios controlados en el documento. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante para visitar el final del documento. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Acepta un visitante para visitar el inicio del documento. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode) | Añade el documento especificado al final de este documento. |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Añade el documento especificado al final de este documento. |
| [Cleanup](./cleanup/)() | Elimina estilos y listas no utilizados del documento. |
| [Cleanup](./cleanup/)(const System::SharedPtr\<Aspose::Words::CleanupOptions\>\&) | Elimina estilos y listas no utilizados del documento según las [CleanupOptions](../cleanupoptions/) dadas. |
| [Clone](./clone/)() | Realiza una copia profunda del [Document](./). |
| [Clone](../node/clone/)(bool) | Crea un duplicado del nodo. |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime) | Compara este documento con otro documento produciendo cambios como número de revisiones de edición y formato [Revision](../revision/). |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compara este documento con otro documento produciendo cambios como número de revisiones de edición y formato [Revision](../revision/). Permite especificar opciones de comparación usando [CompareOptions](../../aspose.words.comparing/compareoptions/). |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::String\&) | Copia estilos de la plantilla especificada a un documento. |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Copia estilos de la plantilla especificada a un documento. |
| [Document](./document/)() | Crea un documento Word en blanco. |
| [Document](./document/)(const System::String\&) | Abre un documento existente desde un archivo. Detecta automáticamente el formato del archivo. |
| [Document](./document/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Abre un documento existente desde un archivo. Permite especificar opciones adicionales como una contraseña de cifrado. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&) | Abre un documento existente desde un flujo. Detecta automáticamente el formato del archivo. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Abre un documento existente desde un flujo. Permite especificar opciones adicionales como una contraseña de cifrado. |
| [Document](./document/)(std::istream\&) |  |
| [Document](./document/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| [EnsureMinimum](./ensureminimum/)() | Si el documento no contiene secciones, crea una sección con un párrafo. |
| [ExpandTableStylesToDirectFormatting](./expandtablestylestodirectformatting/)() | Convierte el formato especificado en estilos de tabla en formato directo en las tablas del documento. |
| [ExtractPages](./extractpages/)(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\>\&) | Devuelve el objeto [Document](./) que representa el rango de páginas especificado y las opciones de extracción de página dadas. |
| [ExtractPages](./extractpages/)(int32_t, int32_t) | Devuelve el objeto [Document](./) que representa el rango de páginas especificado. |
| [get_AttachedTemplate](./get_attachedtemplate/)() | Obtiene o establece la ruta completa de la plantilla adjunta al documento. |
| [get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/)() | Obtiene o establece una bandera que indica si los estilos del documento se actualizan para coincidir con los estilos de la plantilla adjunta cada vez que el documento se abre en MS Word. |
| [get_BackgroundShape](../documentbase/get_backgroundshape/)() const | Obtiene o establece la forma de fondo del documento. Puede ser **null**. |
| [get_Bibliography](./get_bibliography/)() | Obtiene el objeto [Bibliography](./get_bibliography/) que representa la lista de fuentes disponibles en el documento. |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Devuelve una colección que representa todas las propiedades integradas del documento. |
| [get_CompatibilityOptions](./get_compatibilityoptions/)() | Proporciona acceso a las opciones de compatibilidad del documento (es decir, las preferencias del usuario ingresadas en la pestaña **Compatibility** del cuadro de diálogo **Options** en Word). |
| [get_Compliance](./get_compliance/)() | Obtiene la versión de cumplimiento OOXML determinada a partir del contenido del documento cargado. Solo tiene sentido para documentos OOXML. |
| [get_Count](../compositenode/get_count/)() | Obtiene el número de hijos inmediatos de este nodo. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() | Devuelve una colección que representa todas las propiedades personalizadas del documento. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Especifica un identificador de nodo personalizado. |
| [get_CustomXmlParts](./get_customxmlparts/)() const | Obtiene o establece la colección de Custom XML Data Storage Parts. |
| [get_DefaultTabStop](./get_defaulttabstop/)() | Obtiene o establece el intervalo (en puntos) entre los tabuladores predeterminados. |
| [get_DigitalSignatures](./get_digitalsignatures/)() const | Obtiene la colección de firmas digitales de este documento y sus resultados de validación. |
| [get_Document](../documentbase/get_document/)() const override | Obtiene esta instancia. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Proporciona opciones que controlan la numeración y posición de las notas finales en este documento. |
| [get_FieldOptions](./get_fieldoptions/)() | Obtiene un objeto [FieldOptions](../../aspose.words.fields/fieldoptions/) que representa opciones para controlar el manejo de campos en el documento. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Obtiene el primer hijo del nodo. |
| [get_FirstSection](./get_firstsection/)() | Obtiene la primera sección del documento. |
| [get_FontInfos](../documentbase/get_fontinfos/)() const | Proporciona acceso a las propiedades de las fuentes utilizadas en este documento. |
| [get_FontSettings](./get_fontsettings/)() const | Obtiene o establece la configuración de fuentes del documento. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Proporciona opciones que controlan la numeración y posición de las notas al pie en este documento. |
| [get_FootnoteSeparators](../documentbase/get_footnoteseparators/)() const | Proporciona acceso a los separadores de notas al pie/nota final definidos en el documento. |
| [get_Frameset](./get_frameset/)() const | Devuelve una instancia de [Frameset](./get_frameset/) si este documento representa una página de marcos. |
| [get_GlossaryDocument](./get_glossarydocument/)() const | Obtiene o establece el documento de glosario dentro de este documento o plantilla. Un documento de glosario es un almacenamiento para entradas de AutoText, AutoCorrect y Building Block definidas en un documento. |
| [get_GrammarChecked](./get_grammarchecked/)() | Devuelve **true** si el documento ha sido revisado por gramática. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Devuelve **true** si este nodo tiene algún nodo hijo. |
| [get_HasMacros](./get_hasmacros/)() | Devuelve **true** si el documento tiene un proyecto VBA (macros). |
| [get_HasRevisions](./get_hasrevisions/)() | Devuelve **true** si el documento tiene cambios controlados. |
| [get_HyphenationOptions](./get_hyphenationoptions/)() | Proporciona acceso a las opciones de guionización del documento. |
| [get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/)() | Especifica si se deben incluir cuadros de texto, notas al pie y notas finales en las estadísticas de recuento de palabras. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Devuelve **true** ya que este nodo puede tener nodos hijos. |
| [get_JustificationMode](./get_justificationmode/)() | Obtiene o establece el ajuste de espaciado de caracteres de un documento. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Obtiene el último hijo del nodo. |
| [get_LastSection](./get_lastsection/)() | Obtiene la última sección del documento. |
| [get_LayoutOptions](./get_layoutoptions/)() const | Obtiene un objeto [LayoutOptions](../../aspose.words.layout/layoutoptions/) que representa opciones para controlar el proceso de diseño de este documento. |
| [get_Lists](../documentbase/get_lists/)() const | Proporciona acceso al formato de lista utilizado en el documento. |
| [get_MailMerge](./get_mailmerge/)() | Devuelve un objeto [MailMerge](../../aspose.words.mailmerging/mailmerge/) que representa la funcionalidad de combinación de correspondencia para el documento. |
| [get_MailMergeSettings](./get_mailmergesettings/)() | Obtiene o establece el objeto que contiene toda la información de combinación de correspondencia para un documento. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [get_NodeChangingCallback](../documentbase/get_nodechangingcallback/)() | Se llama cuando se inserta o elimina un nodo en el documento. |
| [get_NodeType](./get_nodetype/)() const override | Devuelve [Document](../nodetype/). |
| [get_OriginalFileName](./get_originalfilename/)() const | Obtiene el nombre de archivo original del documento. |
| [get_OriginalLoadFormat](./get_originalloadformat/)() const | Obtiene el formato del documento original que se cargó en este objeto. |
| [get_PackageCustomParts](./get_packagecustomparts/)() const | Obtiene o establece la colección de partes personalizadas (contenido arbitrario) que están vinculadas al paquete OOXML usando "relaciones desconocidas". |
| [get_PageColor](../documentbase/get_pagecolor/)() | Obtiene o establece el color de página del documento. Esta propiedad es una versión más simple de [BackgroundShape](../documentbase/get_backgroundshape/). |
| [get_PageCount](./get_pagecount/)() | Obtiene el número de páginas del documento según lo calculado por la operación de diseño de página más reciente. |
| [get_ParentNode](../node/get_parentnode/)() | Obtiene el padre inmediato de este nodo. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Obtiene el nodo que precede inmediatamente a este nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectionType](./get_protectiontype/)() | Obtiene el tipo de protección de documento actualmente activo. |
| [get_PunctuationKerning](./get_punctuationkerning/)() | Especifica si el kerning se aplica tanto al texto latino como a la puntuación. |
| [get_Range](../node/get_range/)() | Devuelve un objeto [Range](../range/) que representa la porción de un documento que está contenida en este nodo. |
| [get_ReadabilityStatistics](./get_readabilitystatistics/)() | Proporciona información de puntuación de legibilidad para el documento. |
| [get_RemovePersonalInformation](./get_removepersonalinformation/)() | Obtiene o establece una bandera que indica que Microsoft Word eliminará toda la información del usuario de los comentarios, revisiones y propiedades del documento al guardar el documento. |
| [get_ResourceLoadingCallback](../documentbase/get_resourceloadingcallback/)() const | Permite controlar cómo se cargan los recursos externos. |
| [get_Revisions](./get_revisions/)() | Obtiene una colección de revisiones (cambios rastreados) que existen en este documento. |
| [get_RevisionsView](./get_revisionsview/)() const | Obtiene o establece un valor que indica si trabajar con la versión original o revisada de un documento. |
| [get_Sections](./get_sections/)() | Devuelve una colección que representa todas las secciones del documento. |
| [get_ShadeFormData](./get_shadeformdata/)() | Especifica si se activa el sombreado gris en los campos de formulario. |
| [get_ShowGrammaticalErrors](./get_showgrammaticalerrors/)() | Especifica si se muestran los errores gramaticales en este documento. |
| [get_ShowSpellingErrors](./get_showspellingerrors/)() | Especifica si se muestran los errores ortográficos en este documento. |
| [get_SpellingChecked](./get_spellingchecked/)() | Devuelve **true** si el documento ha sido revisado ortográficamente. |
| [get_Styles](../documentbase/get_styles/)() const | Devuelve una colección de estilos definidos en el documento. |
| [get_Theme](./get_theme/)() | Obtiene el objeto [Theme](./get_theme/) para este documento. |
| [get_TrackRevisions](./get_trackrevisions/)() | True si los cambios se rastrean cuando este documento se edita en Microsoft Word. |
| [get_Variables](./get_variables/)() | Devuelve la colección de variables añadidas a un documento o plantilla. |
| [get_VbaProject](./get_vbaproject/)() const | Obtiene o establece un [VbaProject](./get_vbaproject/). |
| [get_VersionsCount](./get_versionscount/)() | Obtiene el número de versiones del documento que se almacenó en el documento DOC. |
| [get_ViewOptions](./get_viewoptions/)() | Proporciona opciones para controlar cómo se muestra el documento en Microsoft Word. |
| [get_WarningCallback](../documentbase/get_warningcallback/)() const | Se llama durante varios procedimientos de procesamiento de documentos cuando se detecta un problema que podría resultar en pérdida de fidelidad de datos o formato. |
| [get_Watermark](./get_watermark/)() | Proporciona acceso a la marca de agua del documento. |
| [get_WebExtensionTaskPanes](./get_webextensiontaskpanes/)() const | Devuelve una colección que representa una lista de complementos del panel de tareas. |
| [get_WriteProtection](./get_writeprotection/)() | Proporciona acceso a las opciones de protección contra escritura del documento. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Obtiene el primer ancestro del [NodeType](../nodetype/) especificado. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Devuelve un nodo hijo N-ésimo que coincide con el tipo especificado. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Devuelve una colección en vivo de nodos hijos que coinciden con el tipo especificado. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Proporciona soporte para la iteración al estilo foreach sobre los nodos hijos de este nodo. |
| [GetPageInfo](./getpageinfo/)(int32_t) | Obtiene el tamaño de página, la orientación y otra información sobre una página que podría ser útil para imprimir o renderizar. |
| [GetText](../compositenode/gettext/)() override | Obtiene el texto de este nodo y de todos sus hijos. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importa un nodo de otro documento al documento actual. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Importa un nodo de otro documento al documento actual con una opción para controlar el formato. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Importa un nodo de otro documento al documento actual con una opción para controlar el formato. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Devuelve el índice del nodo hijo especificado en la matriz de nodos hijos. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Une secuencias con el mismo formato en todos los párrafos del documento. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Un método de utilidad que convierte un valor de enumeración de tipo de nodo en una cadena legible para el usuario. |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Cambia los valores de tipo de campo [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) de [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) en todo el documento para que correspondan a los tipos de campo contenidos en los códigos de campo. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtiene el nodo anterior según el algoritmo de recorrido en preorden del árbol. |
| [Protect](./protect/)(Aspose::Words::ProtectionType) | Protege el documento de cambios sin modificar la contraseña existente o asigna una contraseña aleatoria. |
| [Protect](./protect/)(Aspose::Words::ProtectionType, const System::String\&) | Protege el documento de cambios y opcionalmente establece una contraseña de protección. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Elimina todos los nodos hijos del nodo actual. |
| [RemoveBlankPages](./removeblankpages/)() | Elimina páginas en blanco del documento. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveCustomizations](./removecustomizations/)() | Elimina las personalizaciones de la barra de herramientas y los comandos del teclado del documento. |
| [RemoveExternalSchemaReferences](./removeexternalschemareferences/)() | Elimina referencias externas de esquemas XML de este documento. |
| [RemoveMacros](./removemacros/)() | Elimina todas las macros (el proyecto VBA) así como las barras de herramientas y las personalizaciones de comandos del documento. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Elimina todos los nodos descendientes de [SmartTag](../../aspose.words.markup/smarttag/) del nodo actual. |
| [RenderToScale](./rendertoscale/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Renderiza una página del documento en un objeto **Graphics** a una escala especificada. |
| [RenderToSize](./rendertosize/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Renderiza una página del documento en un objeto **Graphics** a un tamaño especificado. |
| [Save](./save/)(const System::String\&) | Guarda el documento en un archivo. Determina automáticamente el formato de guardado a partir de la extensión. |
| [Save](./save/)(const System::String\&, Aspose::Words::SaveFormat) | Guarda el documento en un archivo en el formato especificado. |
| [Save](./save/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Guarda el documento en un archivo usando las opciones de guardado especificadas. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Guarda el documento en un flujo usando el formato especificado. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Guarda el documento en un flujo usando las opciones de guardado especificadas. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, Aspose::Words::SaveFormat) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) |  |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Selecciona el primer [Node](../node/) que coincide con la expresión XPath. |
| [set_AttachedTemplate](./set_attachedtemplate/)(const System::String\&) | Establecedor de [Aspose::Words::Document::get_AttachedTemplate](./get_attachedtemplate/). |
| [set_AutomaticallyUpdateStyles](./set_automaticallyupdatestyles/)(bool) | Establecedor de [Aspose::Words::Document::get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/). |
| [set_BackgroundShape](../documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Establecedor de [Aspose::Words::DocumentBase::get_BackgroundShape](../documentbase/get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Método setter para [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_CustomXmlParts](./set_customxmlparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPartCollection\>\&) | Establecedor de [Aspose::Words::Document::get_CustomXmlParts](./get_customxmlparts/). |
| [set_DefaultTabStop](./set_defaulttabstop/)(double) | Establecedor de [Aspose::Words::Document::get_DefaultTabStop](./get_defaulttabstop/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Establecedor de [Aspose::Words::Document::get_FontSettings](./get_fontsettings/). |
| [set_GlossaryDocument](./set_glossarydocument/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | Establecedor de [Aspose::Words::Document::get_GlossaryDocument](./get_glossarydocument/). |
| [set_GrammarChecked](./set_grammarchecked/)(bool) | Establecedor de [Aspose::Words::Document::get_GrammarChecked](./get_grammarchecked/). |
| [set_IncludeTextboxesFootnotesEndnotesInStat](./set_includetextboxesfootnotesendnotesinstat/)(bool) | Establecedor de [Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/). |
| [set_JustificationMode](./set_justificationmode/)(Aspose::Words::Settings::JustificationMode) | Establecedor de [Aspose::Words::Document::get_JustificationMode](./get_justificationmode/). |
| [set_MailMergeSettings](./set_mailmergesettings/)(const System::SharedPtr\<Aspose::Words::Settings::MailMergeSettings\>\&) | Establecedor de [Aspose::Words::Document::get_MailMergeSettings](./get_mailmergesettings/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Se llama cuando se inserta o elimina un nodo en el documento. |
| [set_PackageCustomParts](./set_packagecustomparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPartCollection\>\&) | Establecedor de [Aspose::Words::Document::get_PackageCustomParts](./get_packagecustomparts/). |
| [set_PageColor](../documentbase/set_pagecolor/)(System::Drawing::Color) | Establecedor de [Aspose::Words::DocumentBase::get_PageColor](../documentbase/get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PunctuationKerning](./set_punctuationkerning/)(bool) | Establecedor de [Aspose::Words::Document::get_PunctuationKerning](./get_punctuationkerning/). |
| [set_RemovePersonalInformation](./set_removepersonalinformation/)(bool) | Establecedor de [Aspose::Words::Document::get_RemovePersonalInformation](./get_removepersonalinformation/). |
| [set_ResourceLoadingCallback](../documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Permite controlar cómo se cargan los recursos externos. |
| [set_RevisionsView](./set_revisionsview/)(Aspose::Words::RevisionsView) | Establecedor de [Aspose::Words::Document::get_RevisionsView](./get_revisionsview/). |
| [set_ShadeFormData](./set_shadeformdata/)(bool) | Establecedor de [Aspose::Words::Document::get_ShadeFormData](./get_shadeformdata/). |
| [set_ShowGrammaticalErrors](./set_showgrammaticalerrors/)(bool) | Establecedor de [Aspose::Words::Document::get_ShowGrammaticalErrors](./get_showgrammaticalerrors/). |
| [set_ShowSpellingErrors](./set_showspellingerrors/)(bool) | Establecedor de [Aspose::Words::Document::get_ShowSpellingErrors](./get_showspellingerrors/). |
| [set_SpellingChecked](./set_spellingchecked/)(bool) | Establecedor de [Aspose::Words::Document::get_SpellingChecked](./get_spellingchecked/). |
| [set_TrackRevisions](./set_trackrevisions/)(bool) | Establecedor de [Aspose::Words::Document::get_TrackRevisions](./get_trackrevisions/). |
| [set_VbaProject](./set_vbaproject/)(const System::SharedPtr\<Aspose::Words::Vba::VbaProject\>\&) | Establecedor de [Aspose::Words::Document::get_VbaProject](./get_vbaproject/). |
| [set_WarningCallback](../documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Establecedor para [Aspose::Words::DocumentBase::get_WarningCallback](../documentbase/get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&, System::DateTime) | Comienza a marcar automáticamente todos los cambios posteriores que realices en el documento de forma programática como cambios de revisión. |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String\&) | Comienza a marcar automáticamente todos los cambios posteriores que realices en el documento de forma programática como cambios de revisión. |
| [StopTrackRevisions](./stoptrackrevisions/)() | Detiene el marcado automático de los cambios del documento como revisiones. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporta el contenido del nodo a una cadena usando las opciones de guardado especificadas. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Desvincula los campos en todo el documento. |
| [Unprotect](./unprotect/)() | Elimina la protección del documento sin importar la contraseña. |
| [Unprotect](./unprotect/)(const System::String\&) | Elimina la protección del documento si se especifica una contraseña correcta. |
| [UpdateActualReferenceMarks](./updateactualreferencemarks/)() | Actualiza la propiedad [ActualReferenceMark](../../aspose.words.notes/footnote/get_actualreferencemark/) de todas las notas al pie y notas finales en el documento. |
| [UpdateFields](./updatefields/)() | Actualiza los valores de los campos en todo el documento. |
| [UpdateListLabels](./updatelistlabels/)() | Actualiza las etiquetas de lista para todos los elementos de lista en el documento. |
| [UpdatePageLayout](./updatepagelayout/)() | Reconstruye el diseño de página del documento. |
| [UpdateTableLayout](./updatetablelayout/)() | Implementa un enfoque anterior para el recálculo del ancho de columnas de tabla que tiene problemas conocidos. |
| [UpdateThumbnail](./updatethumbnail/)(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) | Actualiza la [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) del documento según las opciones especificadas. |
| [UpdateThumbnail](./updatethumbnail/)() | Actualiza la [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) del documento usando opciones predeterminadas. |
| [UpdateWordCount](./updatewordcount/)() | Actualiza las propiedades de recuento de palabras del documento. |
| [UpdateWordCount](./updatewordcount/)(bool) | Actualiza las propiedades de recuento de palabras del documento, opcionalmente actualiza la propiedad [Lines](../../aspose.words.properties/builtindocumentproperties/get_lines/). |
## Observaciones


El [Document](./) es un objeto central en la biblioteca Aspose.Words.

Para cargar un documento existente en cualquiera de los formatos [LoadFormat](../loadformat/), pasa un nombre de archivo o un flujo a uno de los constructores de [Document](./). Para crear un documento en blanco, llama al constructor sin parámetros.

Utiliza una de las sobrecargas del método Save para guardar el documento en cualquiera de los formatos [SaveFormat](../saveformat/).

Para dibujar páginas del documento directamente sobre un objeto **Graphics**, usa el método [RenderToScale()](../) o [RenderToSize()](../).

Para imprimir el documento, usa uno de los métodos [Print()](../).

[MailMerge](./get_mailmerge/) is the [Aspose.Words](../)'s reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

[Document](./) stores document-wide information such as [Styles](../documentbase/get_styles/), [BuiltInDocumentProperties](./get_builtindocumentproperties/), [CustomDocumentProperties](./get_customdocumentproperties/), lists and macros. Most of these objects are accessible via the corresponding properties of the [Document](./).

El [Document](./) es un nodo raíz de un árbol que contiene todos los demás nodos del documento. El árbol es un patrón de diseño Composite y, en muchos aspectos, es similar a XmlDocument. El contenido del documento puede manipularse libremente de forma programática:

* The nodes of the document can be accessed via typed collections, for example [Sections](./get_sections/), [ParagraphCollection](../paragraphcollection/) etc.
* The nodes of the document can be selected by their node type using [GetChildNodes()](../compositenode/getchildnodes/) or using an XPath query with [SelectNodes()](../) or [SelectSingleNode()](../).
* Content nodes can be added or removed from anywhere in the document using [InsertBefore1()</see>, <see cref="Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertAfter1()](../), [RemoveChild``1()](../) and other methods provided by the base class [CompositeNode](../compositenode/).
* The formatting attributes of each node can be changed via the properties of that node.



Considera usar [DocumentBuilder](../documentbuilder/) que simplifica la tarea de crear o poblar programáticamente el árbol del documento.

El [Document](./) solo puede contener objetos [Section](../section/).

En Microsoft Word, un documento válido necesita tener al menos una sección.
## Ver también

* Class [DocumentBase](../documentbase/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
