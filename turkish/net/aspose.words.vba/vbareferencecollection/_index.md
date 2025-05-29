---
title: VbaReferenceCollection Class
linktitle: VbaReferenceCollection
articleTitle: VbaReferenceCollection
second_title: .NET için Aspose.Words
description: Projelerinizde VbaReference nesnelerini etkili bir şekilde yönetmek için güçlü bir araç olan Aspose.Words.Vba.VbaReferenceCollection sınıfını keşfedin.
type: docs
weight: 7450
url: /tr/net/aspose.words.vba/vbareferencecollection/
---
## VbaReferenceCollection class

Bir koleksiyonu temsil eder[`VbaReference`](../vbareference/) nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[VBA Makrolarıyla Çalışma](https://docs.aspose.com/words/net/working-with-vba-macros/) belgeleme makalesi.

```csharp
public sealed class VbaReferenceCollection : IEnumerable<VbaReference>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.vba/vbareferencecollection/count/) { get; } | Koleksiyondaki VBA referanslarının sayısını döndürür. |
| [Item](../../aspose.words.vba/vbareferencecollection/item/) { get; } | Alır[`VbaReference`](../vbareference/) belirtilen dizindeki nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Remove](../../aspose.words.vba/vbareferencecollection/remove/)(*[VbaReference](../vbareference/)*) | Belirtilen bir öğenin ilk örneğini kaldırır[`VbaReference`](../vbareference/) koleksiyondan bir öğe. |
| [RemoveAt](../../aspose.words.vba/vbareferencecollection/removeat/)(*int*) | Şunu kaldırır:[`VbaReference`](../vbareference/) koleksiyonun belirtilen dizinindeki öğe. |

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

* class [VbaReference](../vbareference/)
* ad alanı [Aspose.Words.Vba](../../aspose.words.vba/)
* toplantı [Aspose.Words](../../)
