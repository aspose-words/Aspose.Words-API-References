---
title: FieldIncludeText
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo INCLUDETEXT.
type: docs
weight: 1900
url: /es/net/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class

Implementa el campo INCLUDETEXT.

```csharp
public class FieldIncludeText : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldIncludeText](fieldincludetext/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldincludetext/bookmarkname/) { get; set; } | Obtiene o establece el nombre del marcador en el documento a incluir. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [Encoding](../../aspose.words.fields/fieldincludetext/encoding/) { get; set; } | Obtiene o establece la codificación aplicada a los datos dentro del archivo al que se hace referencia. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [LockFields](../../aspose.words.fields/fieldincludetext/lockfields/) { get; set; } | Obtiene o establece si se debe evitar que se actualicen los campos del documento incluido. |
| [MimeType](../../aspose.words.fields/fieldincludetext/mimetype/) { get; set; } | Obtiene o establece el tipo MIME del archivo al que se hace referencia. |
| [NamespaceMappings](../../aspose.words.fields/fieldincludetext/namespacemappings/) { get; set; } | Obtiene o establece las asignaciones de espacio de nombres para consultas XPath. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [SourceFullName](../../aspose.words.fields/fieldincludetext/sourcefullname/) { get; set; } | Obtiene o establece la ubicación del documento usando un IRI. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| [TextConverter](../../aspose.words.fields/fieldincludetext/textconverter/) { get; set; } | Obtiene o establece el nombre del convertidor de texto para el formato del archivo incluido. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |
| [XPath](../../aspose.words.fields/fieldincludetext/xpath/) { get; set; } | Obtiene o establece XPath para la parte deseada del archivo XML. |
| [XslTransformation](../../aspose.words.fields/fieldincludetext/xsltransformation/) { get; set; } | Obtiene o establece la ubicación de la transformación XSL para formatear datos XML. |

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

Inserta todo o parte del texto y gráficos contenidos en otro documento.

### Ejemplos

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // A continuación se muestran dos formas de utilizar los campos INCLUDETEXT para mostrar el contenido de un archivo XML en el sistema de archivos local.
    // 1 - Realizar una transformación XSL en un documento XML:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - Usa un XPath para tomar elementos específicos de un documento XML:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");

/// <summary>
/// Utilice un generador de documentos para insertar un campo INCLUDETEXT con propiedades personalizadas.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
