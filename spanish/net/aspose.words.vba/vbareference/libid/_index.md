---
title: VbaReference.LibId
linktitle: LibId
articleTitle: LibId
second_title: Aspose.Words para .NET
description: Descubra la propiedad LibId de VBA y recupere fácilmente el identificador de la biblioteca de tipos de automatización con esta guía esencial para desarrolladores. ¡Mejore sus habilidades de programación!
type: docs
weight: 10
url: /es/net/aspose.words.vba/vbareference/libid/
---
## VbaReference.LibId property

Obtiene un valor de cadena que contiene el identificador de una biblioteca de tipo Automation.

```csharp
public abstract string LibId { get; }
```

## Observaciones

Dependiendo del tipo de referencia, el valor de esta propiedad puede ser:

* una LibidReference especificada en 2.1.1.8 LibidReference de [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office_file_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e258ddf66a5
* una ProjectReference especificada en 2.1.1.12 ProjectReference de [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office_file_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537701aa8131

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

* class [VbaReference](../)
* espacio de nombres [Aspose.Words.Vba](../../../aspose.words.vba/)
* asamblea [Aspose.Words](../../../)
