---
title: FieldHyperlink.IsImageMap
second_title: Справочник по API Aspose.Words для .NET
description: FieldHyperlink свойство. Получает или задает необходимость добавления координат к гиперссылке для карты изображения на стороне сервера.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldhyperlink/isimagemap/
---
## FieldHyperlink.IsImageMap property

Получает или задает необходимость добавления координат к гиперссылке для карты изображения на стороне сервера.

```csharp
public bool IsImageMap { get; set; }
```

### Примеры

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
* пространство имен [Aspose.Words.Fields](../../fieldhyperlink/)
* сборка [Aspose.Words](../../../)


