---
title: FieldHyperlink.IsImageMap
linktitle: IsImageMap
articleTitle: IsImageMap
second_title: Aspose.Words для .NET
description: Узнайте, как свойство FieldHyperlink IsImageMap улучшает ваши серверные карты изображений, добавляя координаты к гиперссылкам для улучшения функциональности.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldhyperlink/isimagemap/
---
## FieldHyperlink.IsImageMap property

Возвращает или задает, следует ли добавлять координаты к гиперссылке для серверной карты изображений.

```csharp
public bool IsImageMap { get; set; }
```

## Примеры

Показывает, как использовать поля HYPERLINK для ссылки на документы в локальной файловой системе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Когда мы нажимаем на это поле ГИПЕРССЫЛКА в Microsoft Word,
// откроется связанный документ, а затем курсор будет установлен на указанной закладке.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Когда мы нажимаем на это поле ГИПЕРССЫЛКА в Microsoft Word,
// откроется связанный документ и автоматически прокрутится вниз до указанного iframe.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### Смотрите также

* class [FieldHyperlink](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
