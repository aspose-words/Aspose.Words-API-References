---
title: VbaReference Class
linktitle: VbaReference
articleTitle: VbaReference
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Vba.VbaReference para una integración perfecta con bibliotecas de tipos de automatización y proyectos VBA. ¡Mejore la automatización de sus documentos hoy mismo!
type: docs
weight: 7440
url: /es/net/aspose.words.vba/vbareference/
---
## VbaReference class

Implementa una referencia a una biblioteca de tipos de automatización o un proyecto VBA.

Para obtener más información, visite el[Trabajar con macros de VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) Artículo de documentación.

```csharp
public abstract class VbaReference
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| abstract [LibId](../../aspose.words.vba/vbareference/libid/) { get; } | Obtiene un valor de cadena que contiene el identificador de una biblioteca de tipo Automation. |
| abstract [Type](../../aspose.words.vba/vbareference/type/) { get; } | Obtiene[`VbaReferenceType`](../vbareferencetype/) objeto que indica el tipo de referencia que un`VbaReference` objeto representa. |

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

* espacio de nombres [Aspose.Words.Vba](../../aspose.words.vba/)
* asamblea [Aspose.Words](../../)
