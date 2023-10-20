---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words для .NET
description: Document ExtractPages метод. ВозвращаетDocument объект представляющий указанный диапазон страниц на С#.
type: docs
weight: 600
url: /ru/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

Возвращает[`Document`](../) объект, представляющий указанный диапазон страниц.

```csharp
public Document ExtractPages(int index, int count)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Индекс первой извлекаемой страницы, отсчитываемый от нуля. |
| count | Int32 | Количество страниц, которые необходимо извлечь. |

## Примечания

Полученный документ должен выглядеть так же, как в MS Word, как если бы мы выполнили «Печать отдельных страниц» — нумерация, колонтитулы и расположение кросс-таблиц сохранятся. Но из-за большого количества нюансов, возникающих при уменьшении количества страниц полное соответствие макета — довольно сложная задача, требующая больших усилий. В зависимости от сложности документа могут быть небольшие различия в макете содержимого итогового документа по сравнению с исходным документом. Любая обратная связь будет полезна будем очень признательны.

## Примеры

Показывает, как получить указанный диапазон страниц из документа.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
