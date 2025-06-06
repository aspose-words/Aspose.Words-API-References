---
title: VbaReference Class
linktitle: VbaReference
articleTitle: VbaReference
second_title: .NET için Aspose.Words
description: Otomasyon türü kitaplıkları ve VBA projeleriyle kusursuz entegrasyon için Aspose.Words.Vba.VbaReference sınıfını keşfedin. Belge otomasyonunuzu bugün geliştirin!
type: docs
weight: 7440
url: /tr/net/aspose.words.vba/vbareference/
---
## VbaReference class

Bir Otomasyon türü kitaplığına veya VBA projesine bir referans uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[VBA Makrolarıyla Çalışma](https://docs.aspose.com/words/net/working-with-vba-macros/) belgeleme makalesi.

```csharp
public abstract class VbaReference
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| abstract [LibId](../../aspose.words.vba/vbareference/libid/) { get; } | Bir Otomasyon türü kitaplığının tanımlayıcısını içeren bir dize değeri alır. |
| abstract [Type](../../aspose.words.vba/vbareference/type/) { get; } | Alır[`VbaReferenceType`](../vbareferencetype/) bir referansın türünü belirten nesne`VbaReference` nesne temsil eder. |

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

* ad alanı [Aspose.Words.Vba](../../aspose.words.vba/)
* toplantı [Aspose.Words](../../)
