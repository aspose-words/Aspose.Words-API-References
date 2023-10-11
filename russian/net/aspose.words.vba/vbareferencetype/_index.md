---
title: Enum VbaReferenceType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Vba.VbaReferenceType перечисление. Позволяет указать типVbaReference объект.
type: docs
weight: 6610
url: /ru/net/aspose.words.vba/vbareferencetype/
---
## VbaReferenceType enumeration

Позволяет указать тип[`VbaReference`](../vbareference/) объект.

```csharp
public enum VbaReferenceType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Registered | `13` | Указывает тип ссылки на библиотеку типов автоматизации. |
| Project | `14` | Указан тип ссылки на внешний проект VBA. |
| Original | `51` | Указывает исходный ссылочный тип библиотеки типов автоматизации. |
| Control | `47` | Указывает измененный ссылочный тип библиотеки типов. |

### Примеры

Показывает, как получить или удалить элемент из коллекции ссылок VBA.

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
/// Возвращает путь от указанного идентификатора библиотеки типов автоматизации.
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
/// Возвращает путь от указанного идентификатора библиотеки типов автоматизации.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### Смотрите также

* пространство имен [Aspose.Words.Vba](../../aspose.words.vba/)
* сборка [Aspose.Words](../../)


