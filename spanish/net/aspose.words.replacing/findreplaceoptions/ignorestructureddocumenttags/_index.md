---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
second_title: Referencia de API de Aspose.Words para .NET
description: FindReplaceOptions propiedad. Obtiene o establece un valor booleano que indica que se debe ignorar el contenido deStructuredDocumentTag . El valor predeterminado esFALSO .
type: docs
weight: 120
url: /es/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

Obtiene o establece un valor booleano que indica que se debe ignorar el contenido de[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) . El valor predeterminado es`FALSO` .

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

### Observaciones

Cuando esta opción está configurada en`verdadero` , el contenido de[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) será tratado como un texto simple.

De lo contrario,[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) se procesará como Story independiente y el patrón de reemplazo se buscará por separado para cada[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/), de modo que si el patrón cruza un[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , entonces no se realizará el reemplazo para dicho patrón.

### Ejemplos

Muestra cómo ignorar el contenido de las etiquetas durante el reemplazo.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// Este párrafo contiene SDT.
Paragraph p = (Paragraph)doc.FirstSection.Body.GetChild(NodeType.Paragraph, 2, true);
string textToSearch = p.ToString(SaveFormat.Text).Trim();

FindReplaceOptions options = new FindReplaceOptions() { IgnoreStructuredDocumentTags = true };
doc.Range.Replace(textToSearch, "replacement", options);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### Ver también

* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../findreplaceoptions/)
* asamblea [Aspose.Words](../../../)


