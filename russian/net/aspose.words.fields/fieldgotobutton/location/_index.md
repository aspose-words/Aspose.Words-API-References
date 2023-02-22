---
title: FieldGoToButton.Location
second_title: Справочник по API Aspose.Words для .NET
description: FieldGoToButton свойство. Получает или задает имя закладки номер страницы или другой элемент для перехода.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

Получает или задает имя закладки, номер страницы или другой элемент для перехода.

```csharp
public string Location { get; set; }
```

### Примеры

Показывает, чтобы вставить поле GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем поле GOTOBUTTON. Когда мы дважды щелкаем это поле в Microsoft Word,
// он наведет текстовый курсор на закладку, на имя которой ссылается свойство Location.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Вставьте допустимую закладку для поля, на которое нужно ссылаться.
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


