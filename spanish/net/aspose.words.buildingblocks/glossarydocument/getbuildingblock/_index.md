---
title: GetBuildingBlock
second_title: Referencia de API de Aspose.Words para .NET
description: Encuentra un bloque de creación utilizando la galería la categoría y el nombre especificados.
type: docs
weight: 70
url: /es/net/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument.GetBuildingBlock method

Encuentra un bloque de creación utilizando la galería, la categoría y el nombre especificados.

```csharp
public BuildingBlock GetBuildingBlock(BuildingBlockGallery gallery, string category, string name)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| gallery | BuildingBlockGallery | Los criterios de la galería. |
| category | String | Los criterios de categoría. Puede ser nulo, en cuyo caso no se utilizará para la comparación. |
| name | String | Los criterios de nombre del bloque de creación. |

### Valor_devuelto

El bloque de creación coincidente o nulo si no se encontró una coincidencia.

### Observaciones

Este es un método conveniente que itera sobre todos los bloques de construcción en esta colección y devuelve el primer bloque de construcción que coincide con la galería, la categoría y el nombre especificados.

Microsoft Word organiza los bloques de construcción en galerías. Las galerías están predefinidas usando el[`BuildingBlockGallery`](../../buildingblockgallery/) enum. Dentro de cada galería, los bloques de creación se pueden organizar en una o más categorías. El nombre de la categoría es una cadena. Cada bloque de construcción tiene un nombre. No se garantiza que un nombre de building block sea único.

### Ejemplos

Muestra formas de acceder a los componentes básicos en un documento de glosario.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 1" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 2" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 3" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 4" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 5" });

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // Hay varias formas de acceder a los bloques de construcción.
    // 1 - Obtener los primeros/últimos bloques de construcción de la colección:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Obtener un bloque de construcción por índice:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Obtenga el primer bloque de construcción que coincida con una galería, nombre y categoría:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Lo haremos usando un visitante personalizado,
    // que le dará a cada BuildingBlock en el GlossaryDocument un GUID único
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // En Microsoft Word, podemos acceder a los bloques de construcción a través de "Insertar" -> "Piezas rápidas" -> "Organizador de bloques de construcción".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Otorga a cada bloque de creación de un documento de glosario visitado un GUID único.
/// Almacena los pares de bloques de creación de GUID en un diccionario.
/// </summary>
public class GlossaryDocVisitor : DocumentVisitor
{
    public GlossaryDocVisitor()
    {
        mBlocksByGuid = new Dictionary<Guid, BuildingBlock>();
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public Dictionary<Guid, BuildingBlock> GetDictionary()
    {
        return mBlocksByGuid;
    }

    public override VisitorAction VisitGlossaryDocumentStart(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Glossary document found!");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGlossaryDocumentEnd(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Reached end of glossary!");
        mBuilder.AppendLine("BuildingBlocks found: " + mBlocksByGuid.Count);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        block.Guid = Guid.NewGuid();
        mBlocksByGuid.Add(block.Guid, block);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.AppendLine("\tVisited block \"" + block.Name + "\"");
        mBuilder.AppendLine("\t Type: " + block.Type);
        mBuilder.AppendLine("\t Gallery: " + block.Gallery);
        mBuilder.AppendLine("\t Behavior: " + block.Behavior);
        mBuilder.AppendLine("\t Description: " + block.Description);

        return VisitorAction.Continue;
    }

    private readonly Dictionary<Guid, BuildingBlock> mBlocksByGuid;
    private readonly StringBuilder mBuilder;
}
```

### Ver también

* class [BuildingBlock](../../buildingblock/)
* enum [BuildingBlockGallery](../../buildingblockgallery/)
* class [GlossaryDocument](../)
* espacio de nombres [Aspose.Words.BuildingBlocks](../../glossarydocument/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
