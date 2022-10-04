---
title: FieldCitation
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo CITATION.
type: docs
weight: 1530
url: /es/net/aspose.words.fields/fieldcitation/
---
## FieldCitation class

Implementa el campo CITATION.

```csharp
public class FieldCitation : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldCitation](fieldcitation/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AnotherSourceTag](../../aspose.words.fields/fieldcitation/anothersourcetag/) { get; set; } | Obtiene o establece un valor que coincide con el **Etiqueta** valor del elemento de otra fuente a incluir en la cita. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [FormatLanguageId](../../aspose.words.fields/fieldcitation/formatlanguageid/) { get; set; } | Obtiene o establece el Id. de idioma que se utiliza junto con el estilo bibliográfico especificado para formatear la cita en el documento. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [PageNumber](../../aspose.words.fields/fieldcitation/pagenumber/) { get; set; } | Obtiene o establece un número de página asociado con la cita. |
| [Prefix](../../aspose.words.fields/fieldcitation/prefix/) { get; set; } | Obtiene o establece un prefijo que se antepone a la cita. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [SourceTag](../../aspose.words.fields/fieldcitation/sourcetag/) { get; set; } | Obtiene o establece un valor que coincide con el **Etiqueta**valor del elemento de la fuente a insertar. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| [Suffix](../../aspose.words.fields/fieldcitation/suffix/) { get; set; } | Obtiene o establece un sufijo que se agrega a la cita. |
| [SuppressAuthor](../../aspose.words.fields/fieldcitation/suppressauthor/) { get; set; } | Obtiene o establece si la información del autor se suprime de la cita. |
| [SuppressTitle](../../aspose.words.fields/fieldcitation/suppresstitle/) { get; set; } | Obtiene o establece si la información del título se suprime de la cita. |
| [SuppressYear](../../aspose.words.fields/fieldcitation/suppressyear/) { get; set; } | Obtiene o establece si la información del año se suprime de la cita. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |
| [VolumeNumber](../../aspose.words.fields/fieldcitation/volumenumber/) { get; set; } | Obtiene o establece un número de volumen asociado a la cita. |

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

Inserta el contenido del **Fuente** elemento con un especificado **Etiqueta** elemento usando un estilo bibliográfico.

### Ejemplos

Muestra cómo trabajar con los campos CITA y BIBLIOGRAFÍA.

```csharp
// Abre un documento que contenga fuentes bibliográficas que podemos encontrar en
// Microsoft Word a través de Referencias -> Citas & Bibliografía -> Administrar fuentes.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Crea una cita con solo el número de página y el autor del libro de referencia.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Nos referimos a las fuentes usando sus nombres de etiqueta.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Crea una cita más detallada que cite dos fuentes.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// Podemos usar un campo BIBLIOGRAFÍA para mostrar todas las fuentes dentro del documento.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "1124";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 1124", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
