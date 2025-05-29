---
title: MailMergeOptions Class
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.MailMergeOptions para soluciones de combinación de correspondencia fluidas y de bajo código. ¡Mejore la automatización de sus documentos con funciones personalizables!
type: docs
weight: 4260
url: /es/net/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class

Representa opciones para la funcionalidad de combinación de correspondencia.

```csharp
public class MailMergeOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [MailMergeOptions](mailmergeoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CleanupOptions](../../aspose.words.lowcode/mailmergeoptions/cleanupoptions/) { get; set; } | Obtiene o establece un conjunto de indicadores que especifican qué elementos deben eliminarse durante la combinación de correspondencia. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.lowcode/mailmergeoptions/cleanupparagraphswithpunctuationmarks/) { get; set; } | Obtiene o establece un valor que indica si los párrafos con signos de puntuación se consideran vacíos y deben eliminarse siRemoveEmptyParagraphs Se especifica la opción. |
| [MergeDuplicateRegions](../../aspose.words.lowcode/mailmergeoptions/mergeduplicateregions/) { get; set; } | Obtiene o establece un valor que indica si todas las regiones de combinación de correspondencia del documento con el nombre de una fuente de datos deben fusionarse durante la ejecución de una combinación de correspondencia con regiones contra la fuente de datos o solo la primera. |
| [MergeWholeDocument](../../aspose.words.lowcode/mailmergeoptions/mergewholedocument/) { get; set; } | Obtiene o establece un valor que indica si los campos de todo el documento se actualizan mientras se ejecuta una combinación de correspondencia con regiones. |
| [PreserveUnusedTags](../../aspose.words.lowcode/mailmergeoptions/preserveunusedtags/) { get; set; } | Obtiene o establece un valor que indica si se deben conservar las etiquetas "bigote" no utilizadas. |
| [RegionEndTag](../../aspose.words.lowcode/mailmergeoptions/regionendtag/) { get; set; } | Obtiene o establece una etiqueta final de región de combinación de correspondencia. |
| [RegionStartTag](../../aspose.words.lowcode/mailmergeoptions/regionstarttag/) { get; set; } | Obtiene o establece una etiqueta de inicio de región de combinación de correspondencia. |
| [RestartListsAtEachSection](../../aspose.words.lowcode/mailmergeoptions/restartlistsateachsection/) { get; set; } | Obtiene o establece un valor que indica si las listas se reinician en cada sección después de ejecutar una combinación de correspondencia. |
| [RetainFirstSectionStart](../../aspose.words.lowcode/mailmergeoptions/retainfirstsectionstart/) { get; set; } | Obtiene o establece un valor que indica si el inicio de la sección de la primera sección del documento y sus copias para las filas de origen de datos posteriores se conservan durante la combinación de correspondencia o se actualizan según el comportamiento de MS Word. |
| [TrimWhitespaces](../../aspose.words.lowcode/mailmergeoptions/trimwhitespaces/) { get; set; } | Obtiene o establece un valor que indica si los espacios iniciales y finales se eliminan de los valores de combinación de correspondencia. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.lowcode/mailmergeoptions/unconditionalmergefieldsandregions/) { get; set; } | Obtiene o establece un valor que indica si los campos de fusión y las regiones de fusión se fusionan independientemente de la condición del campo IF principal. |
| [UseNonMergeFields](../../aspose.words.lowcode/mailmergeoptions/usenonmergefields/) { get; set; } | Cuando`verdadero` , especifica que además de los campos MERGEFIELD, la combinación de correspondencia se realiza en algunos otros tipos de campos y también en las etiquetas "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.lowcode/mailmergeoptions/usewholeparagraphasregion/) { get; set; } | Obtiene o establece un valor que indica si se incluye todo el párrafo con**Inicio de tabla** o**Fin de la tabla** campo o rango particular entre**Inicio de tabla** y**Fin de la tabla** Los campos deben incluirse en la región de combinación de correspondencia. |

## Ejemplos

Muestra cómo realizar la operación de combinación de correspondencia para un solo registro.

```csharp
// Hay varias formas de realizar la operación de combinación de correspondencia:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../)
