---
title: FieldHyperlink.OpenInNewWindow
linktitle: OpenInNewWindow
articleTitle: OpenInNewWindow
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldHyperlink OpenInNewWindow, с легкостью управляйте открытием ссылок в новом окне браузера для улучшения пользовательского опыта.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldhyperlink/openinnewwindow/
---
## FieldHyperlink.OpenInNewWindow property

Возвращает или задает, следует ли открывать целевой сайт в новом окне веб-браузера.

```csharp
public bool OpenInNewWindow { get; set; }
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
