---
title: Class FieldRef
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.FieldRef clase. Implementa el campo REF.
type: docs
weight: 2180
url: /es/net/aspose.words.fields/fieldref/
---
## FieldRef class

Implementa el campo REF.

```csharp
public class FieldRef : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldRef](fieldref/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldref/bookmarkname/) { get; set; } | Obtiene o establece el nombre del marcador al que se hace referencia. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [IncludeNoteOrComment](../../aspose.words.fields/fieldref/includenoteorcomment/) { get; set; } | Obtiene o establece si se incrementan los números de nota al pie, nota al final y anotación que están marcados por el marcador, e inserta el texto correspondiente de nota al pie, nota al final y comentario. |
| [InsertHyperlink](../../aspose.words.fields/fieldref/inserthyperlink/) { get; set; } | Obtiene o establece si se debe crear un hipervínculo al párrafo marcado. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldref/insertparagraphnumber/) { get; set; } | Obtiene o establece si se debe insertar el número de párrafo del párrafo al que se hace referencia exactamente como aparece en el documento. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldref/insertparagraphnumberinfullcontext/) { get; set; } | Obtiene o establece si insertar el número de párrafo del párrafo al que se hace referencia en contexto completo. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldref/insertparagraphnumberinrelativecontext/) { get; set; } | Obtiene o establece si insertar el número de párrafo del párrafo al que se hace referencia en contexto relativo. |
| [InsertRelativePosition](../../aspose.words.fields/fieldref/insertrelativeposition/) { get; set; } | Obtiene o establece si se inserta la posición relativa del párrafo al que se hace referencia. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [NumberSeparator](../../aspose.words.fields/fieldref/numberseparator/) { get; set; } | Obtiene o establece la secuencia de caracteres que se utiliza para separar números de secuencia y números de página. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldref/suppressnondelimiters/) { get; set; } | Obtiene o establece si suprimir los caracteres no delimitadores. |
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

Inserta el texto o los gráficos representados por el marcador especificado.

### Ejemplos

Muestra cómo crear texto marcado con un campo SET y luego mostrarlo en el documento usando un campo REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

  // Nombre el texto marcado con un campo SET.
// Este campo se refiere al "marcador", no a una estructura de marcador que aparece dentro del texto, sino a una variable con nombre.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Hacer referencia al marcador por su nombre en un campo REF y mostrar su contenido.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

Muestra cómo insertar campos REF en marcadores de referencia.

```csharp
public void FieldRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #1");
    builder.Write("Text that will appear in REF field");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #2");
    builder.EndBookmark("MyBookmark");
    builder.MoveToDocumentStart();

    // Aplicaremos un formato de lista personalizado, donde la cantidad de paréntesis angulares indica el nivel de lista en el que nos encontramos actualmente.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Inserte un campo REF que contendrá el texto dentro de nuestro marcador, actuará como un hipervínculo y clonará las notas al pie del marcador.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Inserta un campo REF y muestra si el marcador al que se hace referencia está encima o debajo de él.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Muestra el número de lista del marcador tal como aparece en el documento.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Mostrar el número de lista del marcador, pero con caracteres no delimitadores, como los corchetes angulares, omitidos.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Bajar un nivel de lista.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Mostrar el número de lista del marcador y los números de todos los niveles de lista por encima de él.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Mostrar los números de nivel de lista entre este campo REF y el marcador al que hace referencia.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // Al final del documento, el marcador aparecerá aquí como un elemento de la lista.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");

/// <summary>
/// Obtener el generador de documentos para insertar un campo REF, hacer referencia a un marcador con él y agregar texto antes y después.
/// </summary>
private static FieldRef InsertFieldRef(DocumentBuilder builder, string bookmarkName, string textBefore, string textAfter)
{
    builder.Write(textBefore);
    FieldRef field = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    field.BookmarkName = bookmarkName;
    builder.Write(textAfter);
    return field;
}
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


