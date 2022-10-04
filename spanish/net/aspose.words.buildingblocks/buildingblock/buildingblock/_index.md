---
title: BuildingBlock
second_title: Referencia de API de Aspose.Words para .NET
description: Inicializa una nueva instancia de esta clase.
type: docs
weight: 10
url: /es/net/aspose.words.buildingblocks/buildingblock/buildingblock/
---
## BuildingBlock constructor

Inicializa una nueva instancia de esta clase.

```csharp
public BuildingBlock(GlossaryDocument glossaryDoc)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| glossaryDoc | GlossaryDocument | El documento del propietario. |

### Observaciones

Cuando[`BuildingBlock`](../) se crea, pertenece al documento de glosario especificado, pero aún no forma parte del documento de glosario y[`ParentNode`](../../../aspose.words/node/parentnode/) es`nulo`.

Para anexar[`BuildingBlock`](../) a un[`GlossaryDocument`](../../glossarydocument/) usar [`AppendChild`](../../../aspose.words/compositenode/appendchild/).

### Ejemplos

Muestra cómo agregar un bloque de creación personalizado a un documento.

```csharp
public void CreateAndInsert()
{
    // El glosario de un documento almacena bloques de construcción.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Cree un bloque de creación, asígnele un nombre y luego agréguelo al documento del glosario.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Todos los GUID de bloques de creación nuevos tienen el mismo valor cero de forma predeterminada y podemos asignarles un nuevo valor único.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Las siguientes propiedades clasifican los bloques de construcción
    // en el menú podemos acceder en Microsoft Word mediante "Insertar" -> "Piezas rápidas" -> "Organizador de bloques de construcción".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Antes de que podamos agregar este bloque de construcción a nuestro documento, necesitaremos darle algunos contenidos,
    // lo que haremos usando un visitante de documentos. Este visitante también establecerá una categoría, galería y comportamiento.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // Podemos acceder al bloque que acabamos de hacer del documento del glosario.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // El bloque en sí es una sección que contiene el texto.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);

    // Ahora, podemos insertarlo en el documento como una nueva sección.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // También podemos encontrarlo en el Organizador de bloques de construcción de Microsoft Word y colocarlo manualmente.
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
        // Configure el bloque de creación como una parte rápida y agregue propiedades utilizadas por el organizador de bloques de creación.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Agrega una sección con texto.
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

* class [GlossaryDocument](../../glossarydocument/)
* class [BuildingBlock](../)
* espacio de nombres [Aspose.Words.BuildingBlocks](../../buildingblock/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
