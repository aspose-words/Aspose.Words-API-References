---
title: StyleCollection.ClearQuickStyleGallery
linktitle: ClearQuickStyleGallery
articleTitle: ClearQuickStyleGallery
second_title: Aspose.Words для .NET
description: Легко очищайте стили из вашей галереи быстрых стилей с помощью метода ClearQuickStyleGallery от StyleCollection. Упростите свой процесс дизайна сегодня!
type: docs
weight: 80
url: /ru/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

Удаляет все стили из панели «Галерея быстрых стилей».

```csharp
public void ClearQuickStyleGallery()
```

## Примеры

Показывает, как удалить стили из панели «Галерея стилей».

```csharp
Document doc = new Document();
// Обратите внимание, что удаление стилей на данный момент работает только с форматом DOCX.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### Смотрите также

* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
