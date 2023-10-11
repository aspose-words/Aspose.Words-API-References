---
title: RevisionCollection.Groups
second_title: Referencia de API de Aspose.Words para .NET
description: RevisionCollection propiedad. Colección de grupos de revisión.
type: docs
weight: 20
url: /es/net/aspose.words/revisioncollection/groups/
---
## RevisionCollection.Groups property

Colección de grupos de revisión.

```csharp
public RevisionGroupCollection Groups { get; }
```

### Ejemplos

Muestra cómo trabajar con la colección de revisiones de un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// Esta colección en sí tiene una colección de grupos de revisión.
// Cada grupo es una secuencia de revisiones adyacentes.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Iterar sobre la colección de grupos e imprimir el texto al que se refiere la revisión.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Cada ejecución a la que afecta una revisión obtiene un objeto de revisión correspondiente.
// La colección de revisiones es considerablemente mayor que el formulario condensado que imprimimos arriba.
// dependiendo de en cuántas Ejecuciones hayamos segmentado el documento durante la edición de Microsoft Word.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // Un StyleDefinitionChange afecta estrictamente a los estilos y no a los nodos de documentos. Esto significa "ParentStyle"
        // la propiedad siempre estará en uso, mientras que ParentNode siempre será nulo.
        // Dado que todos los demás cambios afectan a los nodos, ParentNode estará en uso y ParentStyle será nulo.
        if (e.Current.RevisionType == RevisionType.StyleDefinitionChange)
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, style: [{e.Current.ParentStyle.Name}]");
        }
        else
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, contents: [{e.Current.ParentNode.GetText().Trim()}]");
        }
    }
}

// Rechaza todas las revisiones a través de la colección, revirtiendo el documento a su forma original.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Ver también

* class [RevisionGroupCollection](../../revisiongroupcollection/)
* class [RevisionCollection](../)
* espacio de nombres [Aspose.Words](../../revisioncollection/)
* asamblea [Aspose.Words](../../../)


