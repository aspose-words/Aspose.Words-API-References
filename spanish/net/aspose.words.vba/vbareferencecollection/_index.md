---
title: VbaReferenceCollection Class
linktitle: VbaReferenceCollection
articleTitle: VbaReferenceCollection
second_title: Aspose.Words para .NET
description: Explore la clase Aspose.Words.Vba.VbaReferenceCollection, una poderosa herramienta para administrar objetos VbaReference de manera eficiente en sus proyectos.
type: docs
weight: 7450
url: /es/net/aspose.words.vba/vbareferencecollection/
---
## VbaReferenceCollection class

Representa una colección de[`VbaReference`](../vbareference/) objetos.

Para obtener más información, visite el[Trabajar con macros de VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) Artículo de documentación.

```csharp
public sealed class VbaReferenceCollection : IEnumerable<VbaReference>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.vba/vbareferencecollection/count/) { get; } | Devuelve el número de referencias de VBA en la colección. |
| [Item](../../aspose.words.vba/vbareferencecollection/item/) { get; } | Obtiene[`VbaReference`](../vbareference/) objeto en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Remove](../../aspose.words.vba/vbareferencecollection/remove/)(*[VbaReference](../vbareference/)*) | Elimina la primera aparición de un valor especificado[`VbaReference`](../vbareference/) Artículo de la colección. |
| [RemoveAt](../../aspose.words.vba/vbareferencecollection/removeat/)(*int*) | Elimina el[`VbaReference`](../vbareference/) elemento en el índice especificado de la colección. |

## Ejemplos

Muestra cómo obtener/eliminar un elemento de la colección de referencia de VBA.

```csharp
public void RemoveVbaReference()
{
    const string brokenPath = @"X:\broken.dll";
    Document doc = new Document(MyDir + "VBA project.docm");

    VbaReferenceCollection references = doc.VbaProject.References;
    Assert.AreEqual(5 ,references.Count);

    for (int i = references.Count - 1; i >= 0; i--)
    {
        VbaReference reference = doc.VbaProject.References[i];
        string path = GetLibIdPath(reference);

        if (path == brokenPath)
            references.RemoveAt(i);
    }
    Assert.AreEqual(4 ,references.Count);

    references.Remove(references[1]);
    Assert.AreEqual(3 ,references.Count);

    doc.Save(ArtifactsDir + "VbaProject.RemoveVbaReference.docm"); 
}

/// <summary>
 /// Devuelve una cadena que representa la ruta LibId de una referencia especificada.
/// </summary>
private static string GetLibIdPath(VbaReference reference)
{
    switch (reference.Type)
    {
        case VbaReferenceType.Registered:
        case VbaReferenceType.Original:
        case VbaReferenceType.Control:
            return GetLibIdReferencePath(reference.LibId);
        case VbaReferenceType.Project:
            return GetLibIdProjectPath(reference.LibId);
        default:
            throw new ArgumentOutOfRangeException();
    }
}

/// <summary>
/// Devuelve la ruta de un identificador especificado de una biblioteca de tipo de automatización.
/// </summary>
private static string GetLibIdReferencePath(string libIdReference)
{
    if (libIdReference != null)
    {
        string[] refParts = libIdReference.Split('#');
        if (refParts.Length > 3)
            return refParts[3];
    }

    return "";
}

/// <summary>
/// Devuelve la ruta de un identificador especificado de una biblioteca de tipo de automatización.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### Ver también

* class [VbaReference](../vbareference/)
* espacio de nombres [Aspose.Words.Vba](../../aspose.words.vba/)
* asamblea [Aspose.Words](../../)
