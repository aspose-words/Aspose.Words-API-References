---
title: Class FieldDdeAuto
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.FieldDdeAuto clase. Implementa el campo DDEAUTO.
type: docs
weight: 1640
url: /es/net/aspose.words.fields/fieldddeauto/
---
## FieldDdeAuto class

Implementa el campo DDEAUTO.

```csharp
public class FieldDdeAuto : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldDdeAuto](fieldddeauto/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [InsertAsBitmap](../../aspose.words.fields/fieldddeauto/insertasbitmap/) { get; set; } | Obtiene o establece si insertar el objeto vinculado como mapa de bits. |
| [InsertAsHtml](../../aspose.words.fields/fieldddeauto/insertashtml/) { get; set; } | Obtiene o establece si insertar el objeto vinculado como texto en formato HTML. |
| [InsertAsPicture](../../aspose.words.fields/fieldddeauto/insertaspicture/) { get; set; } | Obtiene o establece si insertar el objeto vinculado como una imagen. |
| [InsertAsRtf](../../aspose.words.fields/fieldddeauto/insertasrtf/) { get; set; } | Obtiene o establece si insertar el objeto vinculado en formato de texto enriquecido (RTF). |
| [InsertAsText](../../aspose.words.fields/fieldddeauto/insertastext/) { get; set; } | Obtiene o establece si insertar el objeto vinculado en formato de solo texto. |
| [InsertAsUnicode](../../aspose.words.fields/fieldddeauto/insertasunicode/) { get; set; } | Obtiene o establece si insertar el objeto vinculado como texto Unicode. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLinked](../../aspose.words.fields/fieldddeauto/islinked/) { get; set; } | Obtiene o establece si se reduce el tamaño del archivo al no almacenar datos gráficos con el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [ProgId](../../aspose.words.fields/fieldddeauto/progid/) { get; set; } | Obtiene o establece el tipo de aplicación de la información del enlace. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [SourceFullName](../../aspose.words.fields/fieldddeauto/sourcefullname/) { get; set; } | Obtiene o establece el nombre y la ubicación del archivo de origen. |
| [SourceItem](../../aspose.words.fields/fieldddeauto/sourceitem/) { get; set; } | Obtiene o establece la parte del archivo de origen que se está vinculando. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
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

Para información copiada de otra aplicación, este campo vincula esa información a su archivo fuente original mediante DDE y se actualiza automáticamente.

### Ejemplos

Muestra cómo usar varios tipos de campos para vincular a otros documentos en el sistema de archivos local y mostrar su contenido.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // A continuación hay tres tipos de campos que podemos usar para mostrar contenidos de un documento vinculado en forma de texto.
    // 1 - Un campo de ENLACE:
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", MyDir + "Document.docx", null, true);

    // 2 - Un campo DDE:
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - Un campo DDEAUTO:
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.docx");
}

{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // A continuación se muestran tres tipos de campos que podemos usar para mostrar contenidos de un documento vinculado en forma de imagen.
    // 1 - Un campo de ENLACE:
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "MySpreadsheet.xlsx",
        "Sheet1!R2C2", true);

    // 2 - Un campo DDE:
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - Un campo DDEAUTO:
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
}

/// <summary>
/// Use un generador de documentos para insertar un campo LINK y establezca sus propiedades de acuerdo con los parámetros.
/// </summary>
private static void InsertFieldLink(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool shouldAutoUpdate)
{
    FieldLink field = (FieldLink)builder.InsertField(FieldType.FieldLink, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;

    builder.Writeln("\n");
}

/// <summary>
/// Utilice un generador de documentos para insertar un campo DDE y establezca sus propiedades de acuerdo con los parámetros.
/// </summary>
private static void InsertFieldDde(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs, string progId,
    string sourceFullName, string sourceItem, bool isLinked, bool shouldAutoUpdate)
{
    FieldDde field = (FieldDde)builder.InsertField(FieldType.FieldDDE, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;

    builder.Writeln("\n");
}

/// <summary>
/// Use un generador de documentos para insertar un campo DDEAUTO y establezca sus propiedades de acuerdo con los parámetros.
/// </summary>
private static void InsertFieldDdeAuto(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool isLinked)
{
    FieldDdeAuto field = (FieldDdeAuto)builder.InsertField(FieldType.FieldDDEAuto, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;
}

public enum InsertLinkedObjectAs
{
    // ObjetoEnlazadoComoTexto
    Text,
    Unicode,
    Html,
    Rtf,
    // ObjetoEnlazadoComoImagen
    Picture,
    Bitmap
}
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


