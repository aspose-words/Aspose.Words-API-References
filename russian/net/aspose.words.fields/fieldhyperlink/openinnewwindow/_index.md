---
title: FieldHyperlink.OpenInNewWindow
linktitle: OpenInNewWindow
articleTitle: OpenInNewWindow
second_title: Aspose.Words для .NET
description: FieldHyperlink OpenInNewWindow свойство. Получает или задает следует ли открывать целевой сайт в новом окне веббраузера на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldhyperlink/openinnewwindow/
---
## FieldHyperlink.OpenInNewWindow property

Получает или задает, следует ли открывать целевой сайт в новом окне веб-браузера.

```csharp
public bool OpenInNewWindow { get; set; }
```

## Примеры

Показывает, как использовать поля HYPERLINK для создания ссылок на документы в локальной файловой системе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Когда мы щелкаем это поле ГИПЕРССЫЛКИ в Microsoft Word,
// он откроет связанный документ, а затем поместит курсор на указанную закладку.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Когда мы щелкаем это поле ГИПЕРССЫЛКИ в Microsoft Word,
// он откроет связанный документ и автоматически прокрутит вниз до указанного iframe.
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
