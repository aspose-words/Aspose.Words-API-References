---
title: VbaReferenceCollection Class
linktitle: VbaReferenceCollection
articleTitle: VbaReferenceCollection
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.Vba.VbaReferenceCollection — мощный инструмент для эффективного управления объектами VbaReference в ваших проектах.
type: docs
weight: 7450
url: /ru/net/aspose.words.vba/vbareferencecollection/
---
## VbaReferenceCollection class

Представляет собой коллекцию[`VbaReference`](../vbareference/) объекты.

Чтобы узнать больше, посетите[Работа с макросами VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) документальная статья.

```csharp
public sealed class VbaReferenceCollection : IEnumerable<VbaReference>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.vba/vbareferencecollection/count/) { get; } | Возвращает количество ссылок VBA в коллекции. |
| [Item](../../aspose.words.vba/vbareferencecollection/item/) { get; } | Получает[`VbaReference`](../vbareference/) объект по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Remove](../../aspose.words.vba/vbareferencecollection/remove/)(*[VbaReference](../vbareference/)*) | Удаляет первое вхождение указанного[`VbaReference`](../vbareference/) предмет из коллекции. |
| [RemoveAt](../../aspose.words.vba/vbareferencecollection/removeat/)(*int*) | Удаляет[`VbaReference`](../vbareference/) элемент по указанному индексу коллекции. |

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

* class [VbaReference](../vbareference/)
* пространство имен [Aspose.Words.Vba](../../aspose.words.vba/)
* сборка [Aspose.Words](../../)
