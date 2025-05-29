---
title: FieldSet.BookmarkText
linktitle: BookmarkText
articleTitle: BookmarkText
second_title: Aspose.Words для .NET
description: Узнайте, как легко управлять свойством FieldSet BookmarkText, чтобы настраивать и улучшать свои закладки для лучшей организации и доступности.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldset/bookmarktext/
---
## FieldSet.BookmarkText property

Получает или задает новый текст закладки.

```csharp
public string BookmarkText { get; set; }
```

## Примеры

Показывает, как создать текст с закладками с помощью поля SET, а затем отобразить его в документе с помощью поля REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Назовите заложенный текст с помощью поля SET.
// Это поле ссылается на «закладку», а не на структуру закладки, которая отображается в тексте, а на именованную переменную.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Ссылка на закладку по имени в поле REF и отображение ее содержимого.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

### Смотрите также

* class [FieldSet](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
