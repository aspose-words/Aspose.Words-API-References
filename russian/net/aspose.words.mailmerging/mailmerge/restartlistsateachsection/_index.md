---
title: MailMerge.RestartListsAtEachSection
second_title: Справочник по API Aspose.Words для .NET
description: MailMerge свойство. Получает или задает значение указывающее перезапускаются ли списки в каждом разделе после выполнения слияния.
type: docs
weight: 110
url: /ru/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Получает или задает значение, указывающее, перезапускаются ли списки в каждом разделе после выполнения слияния.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

### Примечания

Значение по умолчанию: **истинный** .

### Примеры

Показывает, как контролировать, перезапускается ли нумерация списков в каждом разделе при выполнении слияния.

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge/)
* сборка [Aspose.Words](../../../)


