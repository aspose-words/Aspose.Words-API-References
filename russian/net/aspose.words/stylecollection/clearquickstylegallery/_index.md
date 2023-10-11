---
title: StyleCollection.ClearQuickStyleGallery
second_title: Справочник по API Aspose.Words для .NET
description: StyleCollection метод. Удаляет все стили с панели Галерея экспрессстилей.
type: docs
weight: 80
url: /ru/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Удаляет все стили с панели «Галерея экспресс-стилей».

```csharp
public void ClearQuickStyleGallery()
```

### Примеры

Показывает, как удалить стили с панели «Галерея стилей».

```csharp
Document doc = new Document();
// Обратите внимание, что стили удаления на данный момент работают только с форматом DOCX.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Смотрите также

* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../stylecollection/)
* сборка [Aspose.Words](../../../)


