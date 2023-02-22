---
title: Enum VbaReferenceType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Vba.VbaReferenceType enumeración. Permite especificar el tipo de unVbaReference objeto.
type: docs
weight: 6300
url: /es/net/aspose.words.vba/vbareferencetype/
---
## VbaReferenceType enumeration

Permite especificar el tipo de un[`VbaReference`](../vbareference/) objeto.

```csharp
public enum VbaReferenceType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Registered | `13` | Especifica un tipo de referencia de biblioteca de tipos de automatización. |
| Project | `14` | Se especificó un tipo de referencia de proyecto VBA externo. |
| Original | `51` | Especifica un tipo de referencia de biblioteca de tipo de automatización original. |
| Control | `47` | Especifica un tipo de referencia de biblioteca de tipos manipulados. |

### Ejemplos

Muestra cómo obtener/eliminar un elemento de la colección de referencia de VBA.

```csharp
[Test]
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
/// Devuelve la ruta de un identificador especificado de una biblioteca de tipos de automatización.
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
/// Devuelve la ruta de un identificador especificado de una biblioteca de tipos de automatización.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### Ver también

* espacio de nombres [Aspose.Words.Vba](../../aspose.words.vba/)
* asamblea [Aspose.Words](../../)


