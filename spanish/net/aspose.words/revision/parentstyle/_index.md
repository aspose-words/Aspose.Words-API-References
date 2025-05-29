---
title: Revision.ParentStyle
linktitle: ParentStyle
articleTitle: ParentStyle
second_title: Aspose.Words para .NET
description: Descubra la propiedad ParentStyle de Revisión, que identifica al propietario inmediato del estilo principal para las revisiones de StyleDefinitionChange. ¡Optimice su proceso de diseño!
type: docs
weight: 50
url: /es/net/aspose.words/revision/parentstyle/
---
## Revision.ParentStyle property

Obtiene el estilo padre inmediato (propietario) de esta revisión. Esta propiedad funcionará solo para elStyleDefinitionChange tipo de revisión.

```csharp
public Style ParentStyle { get; }
```

## Observaciones

Si esta revisión se relaciona con cambios en los nodos del documento, utilice[`ParentNode`](../parentnode/) en su lugar.

## Ejemplos

Muestra cómo trabajar con la colección de revisiones de un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

//Esta colección en sí tiene una colección de grupos de revisión.
//Cada grupo es una secuencia de revisiones adyacentes.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Itera sobre la colección de grupos e imprime el texto al que se refiere la revisión.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Cada ejecución que afecta una revisión obtiene un objeto de revisión correspondiente.
// La colección de revisiones es considerablemente más grande que la forma condensada que imprimimos arriba,
// dependiendo de en cuántas ejecuciones hayamos segmentado el documento durante la edición de Microsoft Word.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        Un StyleDefinitionChange afecta estrictamente a los estilos, no a los nodos del documento. Esto significa que el "ParentStyle"
        // La propiedad siempre estará en uso, mientras que ParentNode siempre será nulo.
        // Dado que todos los demás cambios afectan a los nodos, ParentNode se utilizará a la inversa y ParentStyle será nulo.
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

// Rechazar todas las revisiones a través de la colección, revirtiendo el documento a su forma original.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Ver también

* class [Style](../../style/)
* class [Revision](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
