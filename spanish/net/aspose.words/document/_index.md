---
title: Document
second_title: Referencia de API de Aspose.Words para .NET
description: Representa un documento de Word.
type: docs
weight: 420
url: /es/net/aspose.words/document/
---
## Document class

Representa un documento de Word.

```csharp
public class Document : DocumentBase
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Document](document/#constructor)() | Crea un documento de Word en blanco. |
| [Document](document/#constructor_1)(Stream) | Abre un documento existente de una secuencia. Detecta automáticamente el formato de archivo. |
| [Document](document/#constructor_3)(string) | Abre un documento existente de un archivo. Detecta automáticamente el formato de archivo. |
| [Document](document/#constructor_2)(Stream, LoadOptions) | Abre un documento existente de una secuencia. Permite especificar opciones adicionales como una contraseña de cifrado. |
| [Document](document/#constructor_4)(string, LoadOptions) | Abre un documento existente de un archivo. Permite especificar opciones adicionales como una contraseña de cifrado. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | Obtiene o establece la ruta completa de la plantilla adjunta al documento. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | Obtiene o establece un indicador que indica si los estilos del documento se actualizan para coincidir con los estilos de la plantilla adjunta cada vez que se abre el documento en MS Word. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Obtiene o establece la forma de fondo del documento. Puede ser nulo. |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | Devuelve una colección que representa todas las propiedades de documento integradas del documento. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Obtiene todos los nodos secundarios inmediatos de este nodo. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | Proporciona acceso a las opciones de compatibilidad de documentos (es decir, las preferencias de usuario ingresadas en el **Compatibilidad** pestaña de la **Opciones** diálogo en Word). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | Obtiene la versión de conformidad con OOXML determinada a partir del contenido del documento cargado. Solo tiene sentido para documentos OOXML. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | Devuelve una colección que representa todas las propiedades del documento personalizado del documento. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | Obtiene o establece la colección de elementos de almacenamiento de datos XML personalizados. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | Obtiene o establece el intervalo (en puntos) entre las tabulaciones predeterminadas. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | Obtiene la colección de firmas digitales para este documento y sus resultados de validación. |
| override [Document](../../aspose.words/documentbase/document/) { get; } |  |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | Proporciona opciones que controlan la numeración y el posicionamiento de las notas finales en este documento. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | Obtiene un **Opciones de campo**objeto que representa opciones para controlar el manejo de campos en el documento. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | Obtiene la primera sección del documento. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Proporciona acceso a las propiedades de las fuentes utilizadas en este documento. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | Obtiene o establece la configuración de fuente del documento. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | Proporciona opciones que controlan la numeración y el posicionamiento de las notas al pie en este documento. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | Devuelve un[`Frameset`](./frameset/)instancia si este documento representa una página de marcos. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | Obtiene o establece el documento del glosario dentro de este documento o plantilla. Un documento de glosario es un almacenamiento para las entradas de Autotexto, Autocorrección y Building Block definidas en un documento. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | Devoluciones **verdadero** si se ha comprobado la gramática del documento. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devuelve verdadero si este nodo tiene nodos secundarios. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | Devoluciones **verdadero** si el documento tiene un proyecto VBA (macros). |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | Devoluciones **verdadero** si el documento tiene cambios registrados. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | Proporciona acceso a las opciones de partición de documentos. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devuelve verdadero ya que este nodo puede tener nodos secundarios. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | Obtiene la última sección del documento. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | Obtiene un **Opciones de diseño** objeto que representa opciones para controlar el proceso de maquetación de este documento. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Proporciona acceso al formato de lista utilizado en el documento. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | Devuelve un **Unificación de correo** objeto que representa la funcionalidad de combinación de correspondencia para el documento. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | Obtiene o establece el objeto que contiene toda la información de combinación de correspondencia de un documento. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Llamado cuando se inserta o elimina un nodo en el documento. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | Devoluciones **NodeType.Document** . |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | Obtiene el nombre de archivo original del documento. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | Obtiene el formato del documento original que se cargó en este objeto. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | Obtiene o establece la colección de piezas personalizadas (contenido arbitrario) que están vinculadas al paquete OOXML mediante "relaciones desconocidas". |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Obtiene o establece el color de página del documento. Esta propiedad es una versión más simple de[`BackgroundShape`](../documentbase/backgroundshape/) . |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | Obtiene el número de páginas del documento calculado por la operación de diseño de página más reciente. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | Obtiene el tipo de protección de documentos actualmente activo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | Obtiene o establece un indicador que indica que Microsoft Word eliminará toda la información del usuario de los comentarios, las revisiones y las propiedades del documento al guardar el documento. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Permite controlar cómo se cargan los recursos externos. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | Obtiene una colección de revisiones (cambios registrados) que existen en este documento. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | Obtiene o establece un valor que indica si se trabaja con la versión original o revisada de un documento. |
| [Sections](../../aspose.words/document/sections/) { get; } | Devuelve una colección que representa todas las secciones del documento. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | Especifica si se debe activar el sombreado gris en los campos de formulario. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | Especifica si mostrar errores gramaticales en este documento. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | Especifica si mostrar errores ortográficos en este documento. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | Devoluciones **verdadero** si se ha revisado la ortografía del documento. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Devuelve una colección de estilos definidos en el documento. |
| [Theme](../../aspose.words/document/theme/) { get; } | Obtiene el[`Theme`](./theme/) objeto para este documento. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | **Verdadero** si se realiza un seguimiento de los cambios cuando se edita este documento en Microsoft Word. |
| [Variables](../../aspose.words/document/variables/) { get; } | Devuelve la colección de variables añadidas a un documento o plantilla. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | Obtiene o establece un[`VbaProject`](./vbaproject/) . |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | Obtiene el número de versiones del documento que se almacenó en el documento DOC. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | Proporciona opciones para controlar cómo se muestra el documento en Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Llamado durante varios procedimientos de procesamiento de documentos cuando se detecta un problema que podría resultar en datos o pérdida de fidelidad de formato. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | Proporciona acceso a la marca de agua del documento. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | Devuelve una colección que representa una lista de complementos del panel de tareas. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | Proporciona acceso a las opciones de protección contra escritura del documento. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(DocumentVisitor) | Acepta un visitante. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | Acepta todos los cambios registrados en el documento. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(Document, ImportFormatMode) | Agrega el documento especificado al final de este documento. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(Document, ImportFormatMode, ImportFormatOptions) | Agrega el documento especificado al final de este documento. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | Limpia estilos y listas no utilizados del documento. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(CleanupOptions) | Limpia estilos y listas no utilizados del documento dependiendo de[`CleanupOptions`](../cleanupoptions/) . |
| [Clone](../../aspose.words/document/clone/#clone)() | Realiza una copia profunda del[`Document`](./document/) . |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [Compare](../../aspose.words/document/compare/#compare)(Document, string, DateTime) | Compara este documento con otro documento produciendo cambios como número de ediciones y revisiones de formato[`Revision`](../revision/) . |
| [Compare](../../aspose.words/document/compare/#compare_1)(Document, string, DateTime, CompareOptions) | Compara este documento con otro documento produciendo cambios como una serie de revisiones de edición y formato[`Revision`](../revision/) . Permite especificar opciones de comparación mediante[`CompareOptions`](../../aspose.words.comparing/compareoptions/) . |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(Document) | Copia estilos de la plantilla especificada a un documento. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(string) | Copia estilos de la plantilla especificada a un documento. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reservado para uso del sistema. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | Si el documento no contiene secciones, crea una sección con un párrafo. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | Convierte el formato especificado en los estilos de tabla en formato directo en las tablas del documento. |
| [ExtractPages](../../aspose.words/document/extractpages/)(int, int) | Devuelve el[`Document`](./document/) objeto que representa el rango especificado de páginas. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para la iteración de cada estilo sobre los nodos secundarios de este nodo. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(int) | Obtiene el tamaño de página, la orientación y otra información sobre una página que podría ser útil para imprimir o renderizar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool) | Importa un nodo de otro documento al documento actual. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(Node, bool, ImportFormatMode) | Importa un nodo de otro documento al documento actual con una opción para controlar el formato. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | Une tiradas con el mismo formato en todos los párrafos del documento. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | Cambia los valores del tipo de campo[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) de[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) en todo el documento para que correspondan a los tipos de campo contenidos en los códigos de campo. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Print](../../aspose.words/document/print/#print)() | Imprime todo el documento en la impresora predeterminada. |
| [Print](../../aspose.words/document/print/#print_1)(PrinterSettings) | Imprime el documento de acuerdo con la configuración de impresora especificada, utilizando el controlador de impresión estándar (sin interfaz de usuario). |
| [Print](../../aspose.words/document/print/#print_3)(string) | Imprima todo el documento en la impresora especificada, utilizando el controlador de impresión estándar (sin interfaz de usuario). |
| [Print](../../aspose.words/document/print/#print_2)(PrinterSettings, string) | Imprime el documento de acuerdo con la configuración de impresora especificada, utilizando el controlador de impresión estándar (sin interfaz de usuario) y un nombre de documento. |
| [Protect](../../aspose.words/document/protect/#protect)(ProtectionType) | Protege el documento de cambios sin cambiar la contraseña existente o asigna una contraseña aleatoria. |
| [Protect](../../aspose.words/document/protect/#protect_1)(ProtectionType, string) | Protege el documento de cambios y opcionalmente establece una contraseña de protección. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Elimina el nodo secundario especificado. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | Elimina las referencias del esquema XML externo de este documento. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | Elimina todas las macros (el proyecto VBA), así como las barras de herramientas y las personalizaciones de comandos del documento. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/) nodos descendientes del nodo actual. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(int, Graphics, float, float, float) | Convierte una página de documento en unGraphics objeto a una escala especificada. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(int, Graphics, float, float, float, float) | Convierte una página de documento en unGraphics objeto a un tamaño especificado. |
| [Save](../../aspose.words/document/save/#save_2)(string) | Guarda el documento en un archivo. Determina automáticamente el formato de guardado de la extensión. |
| [Save](../../aspose.words/document/save/#save)(Stream, SaveFormat) | Guarda el documento en una secuencia utilizando el formato especificado. |
| [Save](../../aspose.words/document/save/#save_1)(Stream, SaveOptions) | Guarda el documento en una secuencia usando las opciones de guardado especificadas. |
| [Save](../../aspose.words/document/save/#save_3)(string, SaveFormat) | Guarda el documento en un archivo en el formato especificado. |
| [Save](../../aspose.words/document/save/#save_4)(string, SaveOptions) | Guarda el documento en un archivo usando las opciones de guardado especificadas. |
| [Save](../../aspose.words/document/save/#save_5)(HttpResponse, string, ContentDisposition, SaveOptions) | Envía el documento al navegador del cliente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Selecciona el primer nodo que coincide con la expresión XPath. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(string) | Comienza a marcar automáticamente todos los cambios adicionales que realice en el documento mediante programación como cambios de revisión. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(string, DateTime) | Comienza a marcar automáticamente todos los cambios adicionales que realice en el documento mediante programación como cambios de revisión. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | Detiene el marcado automático de los cambios del documento como revisiones. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | Desvincula campos de todo el documento. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | Elimina la protección del documento independientemente de la contraseña. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(string) | Elimina la protección del documento si se especifica una contraseña correcta. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | Actualiza los valores de los campos en todo el documento. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | Actualiza las etiquetas de la lista para todos los elementos de la lista en el documento. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | Reconstruye el diseño de página del documento. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | Actualizaciones[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) del documento usando las opciones predeterminadas. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(ThumbnailGeneratingOptions) | Actualizaciones[`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) del documento según las opciones especificadas. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | Actualiza las propiedades de recuento de palabras del documento. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(bool) | Actualiza las propiedades de recuento de palabras del documento, opcionalmente actualiza[`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) propiedad. |

### Observaciones

los **Documento** es un objeto central en la biblioteca Aspose.Words.

Para cargar un documento existente en cualquiera de los[`LoadFormat`](../loadformat/) formatos, pase un nombre de archivo o una secuencia a uno de los **Documento** constructores Para crear un documento en blanco, llame al constructor sin parámetros.

Use una de las sobrecargas del método Save para guardar el documento en cualquiera de los [`SaveFormat`](../saveformat/) formatos.

Para dibujar páginas de documentos directamente en un **Gráficos** objeto use [`RenderToScale`](./rendertoscale/) o[`RenderToSize`](./rendertosize/) método.

Para imprimir el documento, utilice uno de los[`Print`](./print/)métodos.

[`MailMerge`](./mailmerge/) es el motor de generación de informes de Aspose.Words que permite poblar informes diseñados en Microsoft Word con datos de varias fuentes de datos de forma rápida y sencilla. Los datos pueden ser de un DataSet, DataTable, DataView, IDataReader o una matriz de valores.  **Unificación de correo** revisará los registros que se encuentran en la fuente de datos y los insertará en los campos de combinación de correo en el documento y lo ampliará según sea necesario.

**Documento** almacena información de todo el documento, como[`Styles`](../documentbase/styles/) , [`BuiltInDocumentProperties`](./builtindocumentproperties/) ,[`CustomDocumentProperties`](./customdocumentproperties/) , listas y macros. La mayoría de estos objetos son accesibles a través de las propiedades correspondientes del **Documento**.

los **Documento**es un nodo raíz de un árbol que contiene todos los demás nodos del documento. El árbol es un patrón de diseño compuesto y, en muchos aspectos, similar a XmlDocument. El contenido del documento se puede manipular libremente mediante programación:

* Se puede acceder a los nodos del documento a través de colecciones escritas, por ejemplo[`Sections`](./sections/) , [`ParagraphCollection`](../paragraphcollection/) etc.
* Los nodos del documento se pueden seleccionar por su tipo de nodo usando [`GetChildNodes`](../compositenode/getchildnodes/) o usando una consulta XPath con[`SelectNodes`](../compositenode/selectnodes/) o[`SelectSingleNode`](../compositenode/selectsinglenode/).
* Los nodos de contenido se pueden agregar o eliminar desde cualquier parte del documento usando [`InsertBefore`](../compositenode/insertbefore/) ,[`InsertAfter`](../compositenode/insertafter/) , [`RemoveChild`](../compositenode/removechild/) y otros métodos proporcionados por la clase base[`CompositeNode`](../compositenode/).
* Los atributos de formato de cada nodo se pueden cambiar a través de las propiedades de ese nodo.

Considere usar[`DocumentBuilder`](../documentbuilder/) eso simplifica la tarea de crear programáticamente o llenar el árbol del documento.

los **Documento** solo puede contener[`Section`](../section/) objetos.

En Microsoft Word, un documento válido debe tener al menos una sección.

### Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con datos de un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // A continuación se muestran dos formas de usar un DataTable como fuente de datos para una combinación de correspondencia.
    // 1: use la tabla completa para la combinación de correspondencia para crear un documento de combinación de correspondencia de salida para cada fila de la tabla:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilice una fila de la tabla para crear un documento de combinación de correspondencia de salida:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento de origen de combinación de correspondencia.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Ver también

* class [DocumentBase](../documentbase/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
