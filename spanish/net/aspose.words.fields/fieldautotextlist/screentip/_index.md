---
title: FieldAutoTextList.ScreenTip
second_title: Referencia de API de Aspose.Words para .NET
description: FieldAutoTextList propiedad. Obtiene o establece el texto de la información en pantalla que se mostrará.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldautotextlist/screentip/
---
## FieldAutoTextList.ScreenTip property

Obtiene o establece el texto de la información en pantalla que se mostrará.

```csharp
public string ScreenTip { get; set; }
```

### Ejemplos

Muestra cómo utilizar un campo AUTOTEXTLIST para seleccionar de una lista de entradas de Autotexto.

```csharp
public void FieldAutoTextList()
{
    Document doc = new Document();

    // Crea un documento de glosario y complétalo con entradas de texto automático.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Cree un campo AUTOTEXTLIST y establezca el texto que mostrará el campo en Microsoft Word.
    // Establece el texto para solicitar al usuario que haga clic con el botón derecho en este campo para seleccionar un bloque de creación de Autotexto,
    // cuyo contenido mostrará el campo.
    FieldAutoTextList field = (FieldAutoTextList)builder.InsertField(FieldType.FieldAutoTextList, true);
    field.EntryName = "Right click here to select an AutoText block";
    field.ListStyle = "Heading 1";
    field.ScreenTip = "Hover tip text for AutoTextList goes here";

    Assert.AreEqual(" AUTOTEXTLIST  \"Right click here to select an AutoText block\" " +
                    "\\s \"Heading 1\" " +
                    "\\t \"Hover tip text for AutoTextList goes here\"", field.GetFieldCode());

    doc.Save(ArtifactsDir + "Field.AUTOTEXTLIST.dotx");
}

/// <summary>
/// Cree un bloque de construcción de tipo Autotexto y agréguelo a un documento de glosario.
/// </summary>
private static void AppendAutoTextEntry(GlossaryDocument glossaryDoc, string name, string contents)
{
    BuildingBlock buildingBlock = new BuildingBlock(glossaryDoc);
    buildingBlock.Name = name;
    buildingBlock.Gallery = BuildingBlockGallery.AutoText;
    buildingBlock.Category = "General";
    buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;

    Section section = new Section(glossaryDoc);
    section.AppendChild(new Body(glossaryDoc));
    section.Body.AppendParagraph(contents);
    buildingBlock.AppendChild(section);

    glossaryDoc.AppendChild(buildingBlock);
}
```

### Ver también

* class [FieldAutoTextList](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldautotextlist/)
* asamblea [Aspose.Words](../../../)


