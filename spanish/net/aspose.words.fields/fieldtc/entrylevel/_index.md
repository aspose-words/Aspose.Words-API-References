---
title: FieldTC.EntryLevel
linktitle: EntryLevel
articleTitle: EntryLevel
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldTC EntryLevel, administre y personalice sin esfuerzo sus niveles de entrada para lograr una mayor eficiencia y flujos de trabajo optimizados.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldtc/entrylevel/
---
## FieldTC.EntryLevel property

Obtiene o establece el nivel de la entrada.

```csharp
public string EntryLevel { get; set; }
```

## Ejemplos

Muestra cómo insertar un campo TOC y filtrar qué campos TC terminan como entradas.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserte un campo TOC, que compilará todos los campos TC en una tabla de contenidos.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Configure el campo solo para recoger entradas TC del tipo "A" y un nivel de entrada entre 1 y 3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    //Estas dos entradas aparecerán en la tabla.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    //Esta entrada se omitirá de la tabla porque tiene un tipo diferente de "A".
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Esta entrada se omitirá de la tabla porque tiene un nivel de entrada fuera del rango 1-3.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// Utilice un generador de documentos para insertar un campo TC.
/// </summary>
public void InsertTocEntry(DocumentBuilder builder, string text, string typeIdentifier, string entryLevel)
{
    FieldTC fieldTc = (FieldTC)builder.InsertField(FieldType.FieldTOCEntry, true);
    fieldTc.OmitPageNumber = true;
    fieldTc.Text = text;
    fieldTc.TypeIdentifier = typeIdentifier;
    fieldTc.EntryLevel = entryLevel;
}
```

### Ver también

* class [FieldTC](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
