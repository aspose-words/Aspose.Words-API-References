---
title: VbaReference.LibId
second_title: Aspose.Words för .NET API Referens
description: VbaReference fast egendom. Hämtar ett strängvärde som innehåller identifieraren för ett bibliotek av automationstyp.
type: docs
weight: 10
url: /sv/net/aspose.words.vba/vbareference/libid/
---
## VbaReference.LibId property

Hämtar ett strängvärde som innehåller identifieraren för ett bibliotek av automationstyp.

```csharp
public abstract string LibId { get; }
```

### Anmärkningar

Beroende på referenstyp kan värdet på den här egenskapen vara:

* en LibidReference specificerad i 2.1.1.8 LibidReference av [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office_file_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e6a58ddf
* en ProjectReference specificerad i 2.1.1.12 ProjectReference av [MS-OVBA]: https://docs.microsoft.com/en-us/openspecs/office_file_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537311aa8

### Exempel

Visar hur man hämtar/tar bort ett element från VBA-referenssamlingen.

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
 /// Returnerar en sträng som representerar LibId-sökvägen för en angiven referens.
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
/// Returnerar sökväg från en specificerad identifierare för ett bibliotek av automationstyp.
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
/// Returnerar sökväg från en specificerad identifierare för ett bibliotek av automationstyp.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### Se även

* class [VbaReference](../)
* namnutrymme [Aspose.Words.Vba](../../vbareference/)
* hopsättning [Aspose.Words](../../../)


