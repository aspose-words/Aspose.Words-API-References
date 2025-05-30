---
title: ImportFormatOptions.KeepSourceNumbering
linktitle: KeepSourceNumbering
articleTitle: KeepSourceNumbering
second_title: Aspose.Words para .NET
description: Controle la numeración de documentos con la propiedad KeepSourceNumbering de ImportFormatOptions. Gestione fácilmente los conflictos para una importación fluida. Valor predeterminado falso.
type: docs
weight: 60
url: /es/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

Obtiene o establece un valor booleano que especifica cómo se importará la numeración cuando entre en conflicto en los documentos de origen y destino. El valor predeterminado es`FALSO` .

```csharp
public bool KeepSourceNumbering { get; set; }
```

## Ejemplos

Muestra cómo resolver un conflicto al importar documentos que tienen listas con el mismo identificador de definición de lista.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Establezca la propiedad "KeepSourceNumbering" en "verdadero" para aplicar un ID de definición de lista diferente
// a estilos idénticos a los que Aspose.Words importa en los documentos de destino.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Muestra cómo importar un documento con listas numeradas.

```csharp
Document srcDoc = new Document(MyDir + "List source.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

Assert.AreEqual(4, dstDoc.Lists.Count);

ImportFormatOptions options = new ImportFormatOptions();

// Si hay un conflicto de estilos de lista, aplique el formato de lista del documento de origen.
// Establezca la propiedad "KeepSourceNumbering" en "falso" para no importar ningún número de lista al documento de destino.
// Establezca la propiedad "KeepSourceNumbering" en "verdadero" e importe todos los conflictos
// estilo de lista de numeración con la misma apariencia que tenía en el documento fuente.
options.KeepSourceNumbering = isKeepSourceNumbering;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);
dstDoc.UpdateListLabels();

Assert.AreEqual(isKeepSourceNumbering ? 5 : 4, dstDoc.Lists.Count);
```

Muestra cómo resolver conflictos de numeración de listas en documentos de origen y destino.

```csharp
// Abra un documento con un esquema de numeración de lista personalizado y luego clónelo.
// Dado que ambos tienen el mismo formato de numeración, los formatos entrarán en conflicto si importamos un documento al otro.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Cuando importamos el clon del documento al original y luego lo agregamos,
// entonces las dos listas con el mismo formato de lista se unirán.
// Si establecemos el indicador "KeepSourceNumbering" en "falso", entonces la lista del clon del documento
// que agreguemos al original continuará con la numeración de la lista a la que lo agreguemos.
// Esto fusionará efectivamente las dos listas en una.
// Si establecemos el indicador "KeepSourceNumbering" en "verdadero", entonces el documento clonado
 // La lista conservará su numeración original, haciendo que las dos listas aparezcan como listas separadas.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### Ver también

* class [ImportFormatOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
