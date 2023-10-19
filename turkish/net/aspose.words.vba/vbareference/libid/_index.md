---
title: VbaReference.LibId
linktitle: LibId
articleTitle: LibId
second_title: Aspose.Words for .NET
description: VbaReference LibId mülk. Otomasyon türü kitaplığının tanımlayıcısını içeren bir dize değeri alır C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.vba/vbareference/libid/
---
## VbaReference.LibId property

Otomasyon türü kitaplığının tanımlayıcısını içeren bir dize değeri alır.

```csharp
public abstract string LibId { get; }
```

## Notlar

Referans türüne bağlı olarak bu özelliğin değeri şu şekilde olabilir:

* 2.1.1.8 [MS-OVBA] LibidReferansında belirtilen bir LibidReferansı: https://docs.microsoft.com/en-us/openspecs/office_file_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e258ddf66a5
* [MS-OVBA]'nın 2.1.1.12 Proje Referansı'nda belirtilen bir Proje Referansı: https://docs.microsoft.com/en-us/openspecs/office_file_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537701aa8131

## Örnekler

VBA referans koleksiyonundan bir öğenin nasıl alınacağını/kaldırılacağını gösterir.

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
 /// Belirtilen bir referansın LibId yolunu temsil eden dizeyi döndürür.
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
/// Otomasyon türü kitaplığının belirtilen tanımlayıcısından yolu döndürür.
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
/// Otomasyon türü kitaplığının belirtilen tanımlayıcısından yolu döndürür.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### Ayrıca bakınız

* class [VbaReference](../)
* ad alanı [Aspose.Words.Vba](../../../aspose.words.vba/)
* toplantı [Aspose.Words](../../../)
