---
title: VbaReference Class
linktitle: VbaReference
articleTitle: VbaReference
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Vba.VbaReference для бесшовной интеграции с библиотеками типов автоматизации и проектами VBA. Улучшите автоматизацию документов сегодня!
type: docs
weight: 7440
url: /ru/net/aspose.words.vba/vbareference/
---
## VbaReference class

Реализует ссылку на библиотеку типов автоматизации или проект VBA.

Чтобы узнать больше, посетите[Работа с макросами VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) документальная статья.

```csharp
public abstract class VbaReference
```

## Характеристики

| Имя | Описание |
| --- | --- |
| abstract [LibId](../../aspose.words.vba/vbareference/libid/) { get; } | Получает строковое значение, содержащее идентификатор библиотеки типов автоматизации. |
| abstract [Type](../../aspose.words.vba/vbareference/type/) { get; } | Получает[`VbaReferenceType`](../vbareferencetype/) объект, который указывает тип ссылки, которую`VbaReference` объект представляет. |

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

* пространство имен [Aspose.Words.Vba](../../aspose.words.vba/)
* сборка [Aspose.Words](../../)
