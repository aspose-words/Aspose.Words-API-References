---
title: VbaReferenceCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: Öğe özelliğiyle VbaReference nesnesine kolayca erişin. Sorunsuz VBA geliştirme için referansları dizine göre verimli bir şekilde alın.
type: docs
weight: 20
url: /tr/net/aspose.words.vba/vbareferencecollection/item/
---
## VbaReferenceCollection indexer

Alır[`VbaReference`](../../vbareference/) belirtilen dizindeki nesne.

```csharp
public VbaReference this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Alınacak referansın sıfır tabanlı indeksi. |

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

* class [VbaReference](../../vbareference/)
* class [VbaReferenceCollection](../)
* ad alanı [Aspose.Words.Vba](../../../aspose.words.vba/)
* toplantı [Aspose.Words](../../../)
