---
title: BuildingBlockType Enum
linktitle: BuildingBlockType
articleTitle: BuildingBlockType
second_title: Aspose.Words para .NET
description: Explora la enumeración BuildingBlockType de Aspose.Words para mejorar la funcionalidad de los documentos en Microsoft Word. ¡Descubre la visibilidad y el comportamiento únicos de los bloques de construcción!
type: docs
weight: 360
url: /es/net/aspose.words.buildingblocks/buildingblocktype/
---
## BuildingBlockType enumeration

Especifica un tipo de bloque de creación. El tipo puede afectar la visibilidad y el comportamiento del bloque de creación en Microsoft Word.

```csharp
public enum BuildingBlockType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | No se especifica información de tipo para el bloque de construcción. |
| AutomaticallyReplaceNameWithContent | `1` | Permite que el bloque de construcción se inserte automáticamente en el documento siempre que se ingrese su nombre en una aplicación. |
| StructuredDocumentTagPlaceholderText | `2` | El bloque de construcción es un texto de marcador de posición de etiqueta de documento estructurado. |
| FormFieldHelpText | `3` | El bloque de construcción es un texto de ayuda del campo de formulario. |
| Normal | `4` | El bloque de construcción es una entrada de documento de glosario normal (es decir, regular). |
| AutoCorrect | `5` | El bloque de construcción está asociado con las herramientas de ortografía y gramática. |
| AutoText | `6` | El bloque de construcción es una entrada de Autotexto. |
| All | `7` | El bloque de construcción está asociado con todos los tipos. |
| Default | `0` | Guardar comoNone . |

## Observaciones

Corresponde a la**Tipo de pieza de documento ST** Escriba en OOXML.

## Ejemplos

Muestra cómo agregar un bloque de construcción personalizado a un documento.

```csharp
public void CreateAndInsert()
{
    // El glosario de un documento almacena bloques de construcción.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Cree un bloque de construcción, asígnele un nombre y luego agréguelo al documento de glosario.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Todos los GUID de bloques de construcción nuevos tienen el mismo valor cero de manera predeterminada, y podemos darles un nuevo valor único.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Las siguientes propiedades categorizan los bloques de construcción
    // en el menú podemos acceder en Microsoft Word a través de “Insertar” -> “Elementos rápidos” -> “Organizador de bloques de construcción”.
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Antes de que podamos agregar este bloque de construcción a nuestro documento, necesitaremos darle algunos contenidos,
    // Lo haremos usando un visitante de documento. Este visitante también definirá una categoría, una galería y un comportamiento.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    // Visita el inicio/fin del BuildingBlock.
    block.Accept(visitor);

    //Podemos acceder al bloque que acabamos de crear desde el documento de glosario.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    //El bloque en sí es una sección que contiene el texto.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);
    //Ahora podemos insertarlo en el documento como una nueva sección.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    //También podemos encontrarlo en el Organizador de bloques de construcción de Microsoft Word y colocarlo manualmente.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Configura un bloque de construcción visitado para insertarlo en el documento como una parte rápida y agrega texto a su contenido.
/// </summary>
public class BuildingBlockVisitor : DocumentVisitor
{
    public BuildingBlockVisitor(GlossaryDocument ownerGlossaryDoc)
    {
        mBuilder = new StringBuilder();
        mGlossaryDoc = ownerGlossaryDoc;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        // Configure el bloque de construcción como una parte rápida y agregue propiedades utilizadas por Building Blocks Organizer.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        //Agrega una sección con texto.
        // Insertar el bloque en el documento agregará esta sección con sus nodos secundarios en la ubicación.
        Section section = new Section(mGlossaryDoc);
        block.AppendChild(section);
        block.FirstSection.EnsureMinimum();

        Run run = new Run(mGlossaryDoc, "Text inside " + block.Name);
        block.FirstSection.Body.FirstParagraph.AppendChild(run);

        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.Append("Visited " + block.Name + "\r\n");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
    private readonly GlossaryDocument mGlossaryDoc;
}
```

### Ver también

* espacio de nombres [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* asamblea [Aspose.Words](../../)
