---
title: IStructuredDocumentTag.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words для .NET
description: Откройте для себя метод IStructuredDocumentTag GetChildNodes, получите доступ к динамической коллекции дочерних узлов, соответствующих указанным вами типам, для улучшенного управления документами.
type: docs
weight: 170
url: /ru/net/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag.GetChildNodes method

Возвращает живую коллекцию дочерних узлов, соответствующих указанным типам.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

## Примеры

Показывает, как удалить структурированный тег документа, но сохранить содержимое внутри.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Эта коллекция предоставляет унифицированный интерфейс для доступа к ранжированным и неранжированным структурированным тегам.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Здесь мы можем получить дочерние узлы из общего интерфейса ранжированных и неранжированных структурированных тегов.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Смотрите также

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* interface [IStructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
