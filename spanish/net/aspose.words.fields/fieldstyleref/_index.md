---
title: FieldStyleRef
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo STYLEREF.
type: docs
weight: 2290
url: /es/net/aspose.words.fields/fieldstyleref/
---
## FieldStyleRef class

Implementa el campo STYLEREF.

```csharp
public class FieldStyleRef : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldStyleRef](fieldstyleref/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldstyleref/insertparagraphnumber/) { get; set; } | Obtiene o establece si se debe insertar el número de párrafo del párrafo al que se hace referencia exactamente como aparece en el documento. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinfullcontext/) { get; set; } | Obtiene o establece si insertar el número de párrafo del párrafo al que se hace referencia en contexto completo. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinrelativecontext/) { get; set; } | Obtiene o establece si insertar el número de párrafo del párrafo al que se hace referencia en contexto relativo. |
| [InsertRelativePosition](../../aspose.words.fields/fieldstyleref/insertrelativeposition/) { get; set; } | Obtiene o establece si se inserta la posición relativa del párrafo al que se hace referencia. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [SearchFromBottom](../../aspose.words.fields/fieldstyleref/searchfrombottom/) { get; set; } | Obtiene o establece si buscar desde la parte inferior de la página actual, en lugar de desde la parte superior. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| [StyleName](../../aspose.words.fields/fieldstyleref/stylename/) { get; set; } | Obtiene o establece el nombre del estilo con el que se formatea el texto a buscar. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldstyleref/suppressnondelimiters/) { get; set; } | Obtiene o establece si suprimir los caracteres no delimitadores. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve **nulo** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza el desvinculado del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se lanza si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Realiza una actualización de campo. Se lanza si el campo ya se está actualizando. |

### Observaciones

STYLEREF se usa para hacer referencia a un fragmento de texto dentro del documento que tiene el formato del estilo especificado.

### Ejemplos

Muestra cómo usar los campos STYLEREF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree una lista basada en una plantilla de lista de Microsoft Word.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// Esta lista generada mostrará "1.a )".
  // El espacio antes del corchete es un carácter no delimitador, que podemos suprimir.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// Agregue texto y aplique estilos de párrafo a los que harán referencia los campos STYLEREF.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Coloque un campo STYLEREF en el encabezado y muestre el primer texto con estilo "List Paragraph" en el documento.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Coloque un campo STYLEREF en el pie de página y haga que muestre el último texto.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// También podemos usar campos STYLEREF para hacer referencia a los números de lista de las listas.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
