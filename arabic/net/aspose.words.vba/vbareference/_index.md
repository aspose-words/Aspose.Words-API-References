---
title: VbaReference Class
linktitle: VbaReference
articleTitle: VbaReference
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Vba.VbaReference للتكامل السلس مع مكتبات أنواع الأتمتة ومشاريع VBA. حسّن أتمتة مستنداتك اليوم!
type: docs
weight: 7440
url: /ar/net/aspose.words.vba/vbareference/
---
## VbaReference class

ينفذ مرجعًا إلى مكتبة نوع الأتمتة أو مشروع VBA.

لمعرفة المزيد، قم بزيارة[العمل مع وحدات الماكرو VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) مقالة توثيقية.

```csharp
public abstract class VbaReference
```

## الخصائص

| اسم | وصف |
| --- | --- |
| abstract [LibId](../../aspose.words.vba/vbareference/libid/) { get; } | يحصل على قيمة سلسلة تحتوي على معرف مكتبة نوع الأتمتة. |
| abstract [Type](../../aspose.words.vba/vbareference/type/) { get; } | يحصل[`VbaReferenceType`](../vbareferencetype/) كائن يشير إلى نوع المرجع الذي`VbaReference` يمثل الكائن. |

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

* مساحة الاسم [Aspose.Words.Vba](../../aspose.words.vba/)
* المجسم [Aspose.Words](../../)
