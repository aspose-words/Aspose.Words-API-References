---
title: FieldShape.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words для .NET
description: Легко управляйте текстом FieldShape — получайте и задавайте значения без усилий для бесперебойного извлечения данных и расширения функциональных возможностей ваших приложений.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldshape/text/
---
## FieldShape.Text property

Получает или задает текст для извлечения.

```csharp
public string Text { get; set; }
```

## Примеры

Показывает, как создавать списки с написанием справа налево, совместимые с языками, с полями BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле BIDIOUTLINE нумерует абзацы, как поля AUTONUM/LISTNUM,
// но виден только при включенном языке редактирования с письмом справа налево, например иврите или арабском.
// В следующем поле будет отображаться «.1», эквивалент RTL номера списка «1.».
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Добавьте еще два поля BIDIOUTLINE, которые будут отображать «.2» и «.3».
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Устанавливаем горизонтальное выравнивание текста для каждого абзаца в документе на RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Если мы включим в Microsoft Word язык редактирования с написанием справа налево, в наших полях будут отображаться числа.
// В противном случае будет отображаться «###».
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

Показывает, как некоторые старые поля Microsoft Word, такие как SHAPE и EMBED, обрабатываются во время загрузки.

```csharp
// Откройте документ, созданный в Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Если мы откроем документ Word и нажмем Alt+F9, мы увидим поле SHAPE и EMBED.
// Поле SHAPE — это якорь/холст для объекта AutoShape с включенным стилем обтекания «В соответствии с текстом».
// Поле EMBED имеет ту же функцию, но для внедренного объекта,
// например, электронную таблицу из внешнего документа Excel.
// Однако эти поля не будут отображаться в коллекции полей документа.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Эти поля поддерживаются только старыми версиями Microsoft Word.
// Процесс загрузки документа преобразует эти поля в объекты Shape,
// к которому мы можем получить доступ в коллекции узлов документа.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// Первый узел Shape соответствует полю SHAPE во входном документе,
// который является встроенным холстом для автофигуры.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// Второй узел Shape — это сама AutoShape.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// Третья форма — это поле EMBED, содержащее внешнюю электронную таблицу.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Смотрите также

* class [FieldShape](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
