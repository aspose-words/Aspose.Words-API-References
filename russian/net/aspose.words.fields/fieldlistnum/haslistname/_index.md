---
title: FieldListNum.HasListName
second_title: Справочник по API Aspose.Words для .NET
description: FieldListNum свойство. Возвращает значение указывающее предоставлено ли имя абстрактного определения нумерации кодом поля.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldlistnum/haslistname/
---
## FieldListNum.HasListName property

Возвращает значение, указывающее, предоставлено ли имя абстрактного определения нумерации кодом поля.

```csharp
public bool HasListName { get; }
```

### Примеры

Показывает, как нумеровать абзацы с помощью полей LISTNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поля LISTNUM отображают число, которое увеличивается в каждом поле LISTNUM.
// Эти поля также имеют множество опций, которые позволяют нам использовать их для эмуляции нумерованных списков.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Списки по умолчанию начинают отсчет с 1, но мы можем установить для этого числа другое значение, например 0.
// В этом поле будет отображаться «0)».
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // Поля LISTNUM поддерживают отдельные счетчики для каждого уровня списка.
// Вставка поля LISTNUM в тот же абзац, что и другое поле LISTNUM
// увеличивает уровень списка вместо счетчика.
// Следующее поле продолжит отсчет, который мы начали выше, и отобразит значение «1» на уровне списка 1.
builder.InsertField(FieldType.FieldListNum, true);

// В этом поле начнется отсчет на уровне списка 2. В нем будет отображаться значение «1».
builder.InsertField(FieldType.FieldListNum, true);

// В этом поле начнется отсчет на уровне списка 3. В нем будет отображаться значение «1».
// Разные уровни списка имеют разное форматирование,
// поэтому в совокупности эти поля будут отображать значение "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Следующее поле LISTNUM, которое мы вставим, продолжит подсчет на уровне списка
// что предыдущее поле LISTNUM было включено.
// Мы можем использовать свойство ListLevel для перехода на другой уровень списка.
// Если бы это поле LISTNUM оставалось на уровне списка 3, оно бы отображало "ii)",
// но, поскольку мы переместили его на уровень списка 2, он продолжает подсчет на этом уровне и отображает "b)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Мы можем установить свойство ListName, чтобы поле эмулировало другой тип поля AUTONUM.
// «NumberDefault» эмулирует AUTONUM, «OutlineDefault» эмулирует AUTONUMOUT,
// и «LegalDefault» эмулирует поля AUTONUMLGL.
// Имя списка «OutlineDefault» с 1 в качестве начального номера приведет к отображению «I.».
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// ListName не переносится из предыдущего поля, поэтому нам нужно будет установить его для каждого нового поля.
// В этом поле продолжается отсчет с другим именем списка и отображается «II.».
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Смотрите также

* class [FieldListNum](../)
* пространство имен [Aspose.Words.Fields](../../fieldlistnum/)
* сборка [Aspose.Words](../../../)


