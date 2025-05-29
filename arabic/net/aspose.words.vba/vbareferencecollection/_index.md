---
title: VbaReferenceCollection Class
linktitle: VbaReferenceCollection
articleTitle: VbaReferenceCollection
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.Vba.VbaReferenceCollection، وهي أداة قوية لإدارة كائنات VbaReference بكفاءة في مشاريعك.
type: docs
weight: 7450
url: /ar/net/aspose.words.vba/vbareferencecollection/
---
## VbaReferenceCollection class

يمثل مجموعة من[`VbaReference`](../vbareference/) الأشياء.

لمعرفة المزيد، قم بزيارة[العمل مع وحدات الماكرو VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) مقالة توثيقية.

```csharp
public sealed class VbaReferenceCollection : IEnumerable<VbaReference>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.vba/vbareferencecollection/count/) { get; } | إرجاع عدد مراجع VBA في المجموعة. |
| [Item](../../aspose.words.vba/vbareferencecollection/item/) { get; } | يحصل[`VbaReference`](../vbareference/) الكائن في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Remove](../../aspose.words.vba/vbareferencecollection/remove/)(*[VbaReference](../vbareference/)*) | يزيل أول ظهور لعنصر محدد[`VbaReference`](../vbareference/) عنصر من المجموعة. |
| [RemoveAt](../../aspose.words.vba/vbareferencecollection/removeat/)(*int*) | يزيل[`VbaReference`](../vbareference/) عنصر في الفهرس المحدد للمجموعة. |

## أمثلة

يوضح كيفية الحصول على عنصر أو إزالته من مجموعة مرجع VBA.

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
 /// إرجاع سلسلة تمثل مسار LibId لمرجع محدد.
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
/// إرجاع المسار من معرف محدد لمكتبة نوع الأتمتة.
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
/// إرجاع المسار من معرف محدد لمكتبة نوع الأتمتة.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### أنظر أيضا

* class [VbaReference](../vbareference/)
* مساحة الاسم [Aspose.Words.Vba](../../aspose.words.vba/)
* المجسم [Aspose.Words](../../)
