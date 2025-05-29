---
title: FieldGoToButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words для .NET
description: Настройте свойство DisplayText вашего FieldGoToButton, чтобы улучшить пользовательский опыт. Легко настройте текст кнопки для бесперебойной навигации по документу и быстрого доступа.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Возвращает или задает текст «кнопки», которая отображается в документе, чтобы ее можно было выбрать для активации перехода.

```csharp
public string DisplayText { get; set; }
```

## Примеры

Показывает, как вставить поле GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавить поле GOTOBUTTON. Когда мы дважды щелкаем это поле в Microsoft Word,
// он переместит текстовый курсор на закладку, на имя которой ссылается свойство Location.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Вставьте допустимую закладку для поля, на которое нужно сослаться.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### Смотрите также

* class [FieldGoToButton](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
