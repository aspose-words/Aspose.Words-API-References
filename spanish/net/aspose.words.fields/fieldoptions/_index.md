---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words para .NET
description: Aspose.Words.Fields.FieldOptions clase. Representa opciones para controlar el manejo de campos en un documento en C#.
type: docs
weight: 2250
url: /es/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Representa opciones para controlar el manejo de campos en un documento.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) artículo de documentación.

```csharp
public sealed class FieldOptions
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Obtiene o configura un generador de código de barras personalizado. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | Obtiene o establece un proveedor que devuelve un estilo de bibliografía para el[`FieldBibliography`](../fieldbibliography/) y[`FieldCitation`](../fieldcitation/) campos. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Obtiene o establece rutas de las plantillas integradas de MS Word. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Obtiene o establece el evaluador de expresiones de comparación de campos. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Obtiene o establece la información del usuario actual. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Obtiene o establece un separador de estilo personalizado para el modificador \t[`FieldToc`](../fieldtoc/) campo. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Obtiene o establece el nombre del autor del documento predeterminado. Si el nombre del autor ya está especificado en las propiedades integradas del documento, esta opción no se considera. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Obtiene o establece un proveedor que devuelve un resultado de consulta para el[`FieldDatabase`](../fielddatabase/) campo. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Obtiene o establece un[`FieldIndexFormat`](./fieldindexformat/) que representa el formato para el[`FieldIndex`](../fieldindex/) campos en el documento. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Obtiene o establece un proveedor que devuelve un objeto cultural específico para cada campo en particular. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Especifica qué cultura usar para formatear el resultado del campo. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Obtiene o establece[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) implementación |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Obtiene o establece[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) implementación. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Obtiene o establece el nombre de archivo del documento. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Obtiene o establece el valor que indica si el texto bidireccional es totalmente compatible durante la actualización del campo o no. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Obtiene o establece el valor que indica si el formato de número heredado (anterior a AW 13.10) para los campos está habilitado o no. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Obtiene o establece la cultura para preprocesar los valores de campo. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Permite controlar cómo se formatea el resultado del campo. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Obtiene o establece el nombre de archivo de la plantilla utilizada por el documento. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Obtiene o establece la tabla de categorías de autoridades. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Obtiene o establece el valor que indica que el formato del número se analiza utilizando una cultura invariante o no |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Obtiene o configura el encuestado según las indicaciones del usuario durante la actualización del campo. |

## Ejemplos

Muestra cómo especificar el origen de la referencia cultural utilizada para el formato de fecha durante una actualización de campo o combinación de correspondencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta dos campos combinados con configuración regional alemana.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Establece la cultura actual en inglés de EE. UU. después de preservar su valor original en una variable.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Esta combinación utilizará la cultura del hilo actual para formatear la fecha, inglés de EE. UU.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configure la siguiente combinación para obtener su valor cultural del código de campo. El valor de esa cultura será el alemán.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// El primer resultado de la fusión contiene una fecha formateada en inglés, mientras que el segundo está en alemán.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Restaura la cultura original del hilo.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Ver también

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
