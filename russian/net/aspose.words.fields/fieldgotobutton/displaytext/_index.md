---
title: FieldGoToButton.DisplayText
second_title: Справочник по API Aspose.Words для .NET
description: FieldGoToButton свойство. Получает или задает текст кнопки которая появляется в документе чтобы ее можно было выбрать для активации перехода.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Получает или задает текст «кнопки», которая появляется в документе, чтобы ее можно было выбрать для активации перехода.

```csharp
public string DisplayText { get; set; }
```

### Примеры

Показывает, что нужно вставить поле GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем поле GOTOBUTTON. Когда мы дважды щелкаем это поле в Microsoft Word,
// он переместит текстовый курсор на закладку, на имя которой ссылается свойство Location.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Вставляем действительную закладку для поля, на которое нужно ссылаться.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### Смотрите также

* class [FieldGoToButton](../)
* пространство имен [Aspose.Words.Fields](../../fieldgotobutton/)
* сборка [Aspose.Words](../../../)


