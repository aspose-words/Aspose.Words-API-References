---
title: VbaProject.References
linktitle: References
articleTitle: References
second_title: Aspose.Words для .NET
description: Изучите свойство VBA Project References, чтобы эффективно управлять ссылками на проекты VBA и улучшить свои возможности кодирования. Раскройте свой потенциал программирования!
type: docs
weight: 70
url: /ru/net/aspose.words.vba/vbaproject/references/
---
## VbaProject.References property

Получает коллекцию ссылок на проекты VBA.

```csharp
public VbaReferenceCollection References { get; }
```

## Примеры

Показывает, как получить/удалить элемент из коллекции ссылок VBA.

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
 /// Возвращает строку, представляющую путь LibId указанной ссылки.
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
/// Возвращает путь из указанного идентификатора библиотеки типов автоматизации.
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
/// Возвращает путь из указанного идентификатора библиотеки типов автоматизации.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### Смотрите также

* class [VbaReferenceCollection](../../vbareferencecollection/)
* class [VbaProject](../)
* пространство имен [Aspose.Words.Vba](../../../aspose.words.vba/)
* сборка [Aspose.Words](../../../)
