---
title: ListCollection.AddSingleLevelList
linktitle: AddSingleLevelList
articleTitle: AddSingleLevelList
second_title: Aspose.Words для .NET
description: С легкостью создавайте и добавляйте одноуровневые списки в документ с помощью метода ListCollection AddSingleLevelList, улучшая организацию и ясность.
type: docs
weight: 60
url: /ru/net/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection.AddSingleLevelList method

Создает новый одноуровневый список на основе предопределенного шаблона и добавляет его в коллекцию списков в документе.

```csharp
public List AddSingleLevelList(ListTemplate listTemplate)
```

## Примеры

Показывает, как создать новый одноуровневый список на основе предопределенного шаблона.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ListCollection listCollection = doc.Lists;

// Создает маркированный список из шаблона BulletCircle.
List bulletedList = listCollection.AddSingleLevelList(ListTemplate.BulletCircle);

// Записывает маркированный список в результирующий документ.
builder.Writeln("Bulleted list starts below:");
builder.ListFormat.List = bulletedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Создает нумерованный список из шаблона NumberUppercaseLetterDot.
List numberedList = listCollection.AddSingleLevelList(ListTemplate.NumberUppercaseLetterDot);

// Записывает нумерованный список в результирующий документ.
builder.Writeln("Numbered list starts below:");
builder.ListFormat.List = numberedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Save(ArtifactsDir + "Lists.AddSingleLevelList.docx");
```

### Смотрите также

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
