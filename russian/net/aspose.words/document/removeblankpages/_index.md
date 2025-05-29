---
title: Document.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words для .NET
description: С легкостью улучшайте свои документы с помощью метода RemoveBlankPages, удаляя нежелательные пустые страницы и придавая им безупречный профессиональный вид.
type: docs
weight: 700
url: /ru/net/aspose.words/document/removeblankpages/
---
## Document.RemoveBlankPages method

Удаляет пустые страницы из документа.

```csharp
public List<int> RemoveBlankPages()
```

### Возвращаемое значение

Список номеров страниц был признан пустым и удален.

## Примечания

Полученный документ не будет содержать страниц, которые считаются пустыми, в то время как остальное содержимое, включая нумерацию, верхние/нижние колонтитулы и общую компоновку, должно остаться неизменным. Страница считается пустой, если в теле страницы нет видимого содержимого, например, пустая таблица без границ будет считаться невидимой, и поэтому страница будет определена как пустая.

## Примеры

Показывает, как удалить пустые страницы из документа.

```csharp
Document doc = new Document(MyDir + "Blank pages.docx");
Assert.AreEqual(2, doc.PageCount);
doc.RemoveBlankPages();
doc.UpdatePageLayout();
Assert.AreEqual(1, doc.PageCount);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
