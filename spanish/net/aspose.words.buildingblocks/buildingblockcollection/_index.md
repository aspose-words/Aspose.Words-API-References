---
title: BuildingBlockCollection Class
linktitle: BuildingBlockCollection
articleTitle: BuildingBlockCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words BuildingBlockCollection, una poderosa herramienta para administrar objetos BuildingBlock de documentos de manera eficiente y mejorar su flujo de trabajo.
type: docs
weight: 340
url: /es/net/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class

Una colección de[`BuildingBlock`](../buildingblock/) objetos en el documento.

Para obtener más información, visite el[Modelo de objetos de documento (DOM) de Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Artículo de documentación.

```csharp
public class BuildingBlockCollection : NodeCollection
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtiene el número de nodos en la colección. |
| [Item](../../aspose.words.buildingblocks/buildingblockcollection/item/) { get; } | Recupera un bloque de construcción en el índice dado. (2 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | Agrega un nodo al final de la colección. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | Determina si un nodo está en la colección. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Proporciona una iteración simple al estilo "foreach" sobre la colección de nodos. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | Devuelve el índice basado en cero del nodo especificado. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | Inserta un nodo en la colección en el índice especificado. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](../../aspose.words.buildingblocks/buildingblockcollection/toarray/#toarray)() | Copia todos los bloques de construcción de la colección a una nueva matriz de bloques de construcción. (2 methods) |

## Observaciones

No se crean instancias de esta clase directamente. Para acceder a una colección de bloques de construcción, utilice el[`BuildingBlocks`](../glossarydocument/buildingblocks/) propiedad.

## Ejemplos

Muestra formas de acceder a los bloques de construcción en un documento de glosario.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    BuildingBlock child1 = new BuildingBlock(glossaryDoc) { Name = "Block 1" };
    glossaryDoc.AppendChild(child1);
    BuildingBlock child2 = new BuildingBlock(glossaryDoc) { Name = "Block 2" };
    glossaryDoc.AppendChild(child2);
    BuildingBlock child3 = new BuildingBlock(glossaryDoc) { Name = "Block 3" };
    glossaryDoc.AppendChild(child3);
    BuildingBlock child4 = new BuildingBlock(glossaryDoc) { Name = "Block 4" };
    glossaryDoc.AppendChild(child4);
    BuildingBlock child5 = new BuildingBlock(glossaryDoc) { Name = "Block 5" };
    glossaryDoc.AppendChild(child5);

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    //Hay varias formas de acceder a los bloques de construcción.
    // 1 - Obtener el primer/último bloque de construcción de la colección:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Obtener un bloque de construcción por índice:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Obtener el primer bloque de construcción que coincida con una galería, nombre y categoría:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Lo haremos usando un visitante personalizado,
    // que le dará a cada BuildingBlock en el GlossaryDocument un GUID único
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    // Visita el inicio/fin del documento Glosario.
    glossaryDoc.Accept(visitor);
    // Visita solo el inicio del documento Glosario.
    glossaryDoc.AcceptStart(visitor);
    // Visita sólo el final del documento Glosario.
    glossaryDoc.AcceptEnd(visitor);
    Console.WriteLine(visitor.GetText());

    // En Microsoft Word, podemos acceder a los bloques de construcción a través de "Insertar" -> "Elementos rápidos" -> "Organizador de bloques de construcción".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Le otorga a cada bloque de construcción en un documento de glosario visitado un GUID único.
/// Almacena los pares de bloques de construcción GUID en un diccionario.
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

* class [NodeCollection](../../aspose.words/nodecollection/)
* espacio de nombres [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* asamblea [Aspose.Words](../../)
