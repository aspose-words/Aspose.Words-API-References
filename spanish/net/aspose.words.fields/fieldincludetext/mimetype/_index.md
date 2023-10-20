---
title: FieldIncludeText.MimeType
linktitle: MimeType
articleTitle: MimeType
second_title: Aspose.Words para .NET
description: FieldIncludeText MimeType propiedad. Obtiene o establece el tipo MIME del archivo al que se hace referencia en C#.
type: docs
weight: 50
url: /es/net/aspose.words.fields/fieldincludetext/mimetype/
---
## FieldIncludeText.MimeType property

Obtiene o establece el tipo MIME del archivo al que se hace referencia.

```csharp
public string MimeType { get; set; }
```

## Ejemplos

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

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

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

* class [FieldIncludeText](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
