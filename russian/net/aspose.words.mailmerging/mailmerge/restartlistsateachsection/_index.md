---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MailMerge RestartListsAtEachSection — управляйте сбросом списков в каждом разделе для бесшовных слияний почты. Повысьте точность вашего документа сегодня!
type: docs
weight: 110
url: /ru/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Возвращает или задает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния почты.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## Примечания

Значение по умолчанию:`истинный` .

## Примеры

Показывает, как контролировать, будет ли нумерация списка начинаться заново в каждом разделе при выполнении слияния почты.

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
