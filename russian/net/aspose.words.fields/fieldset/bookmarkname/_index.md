---
title: FieldSet.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words для .NET
description: FieldSet BookmarkName свойство. Получает или задает имя закладки на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldset/bookmarkname/
---
## FieldSet.BookmarkName property

Получает или задает имя закладки.

```csharp
public string BookmarkName { get; set; }
```

## Примеры

Показывает, как создать текст с закладкой с помощью поля SET, а затем отобразить его в документе с помощью поля REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Назовите текст закладки с помощью поля SET.
// Это поле относится к «закладке», а не к структуре закладки, которая появляется в тексте, а к именованной переменной.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Обращаемся к закладке по имени в поле REF и отображаем ее содержимое.
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
