---
title: FieldAutoTextList.ListStyle
linktitle: ListStyle
articleTitle: ListStyle
second_title: Aspose.Words para .NET
description: Descubre la propiedad FieldAutoTextList ListStyle para personalizar tus listas de entradas fácilmente. ¡Mejora tu contenido con estilos personalizados hoy mismo!
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldautotextlist/liststyle/
---
## FieldAutoTextList.ListStyle property

Obtiene o establece el nombre del estilo en el que se basa la lista que contendrá las entradas.

```csharp
public string ListStyle { get; set; }
```

## Ejemplos

Muestra cómo utilizar un campo LISTAAUTOTEXTO para seleccionar de una lista de entradas de Autotexto.

```csharp
public void FieldAutoTextList()
{
    Document doc = new Document();

    // Cree un documento de glosario y rellénelo con entradas de texto automáticas.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Cree un campo LISTAAUTOTEXTO y configure el texto que el campo mostrará en Microsoft Word.
    // Establezca el texto que debe solicitar al usuario que haga clic derecho en este campo para seleccionar un bloque de creación de Autotexto.
    //cuyo contenido mostrará el campo.
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
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
