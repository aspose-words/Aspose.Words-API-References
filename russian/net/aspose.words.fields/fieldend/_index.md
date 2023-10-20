---
title: FieldEnd Class
linktitle: FieldEnd
articleTitle: FieldEnd
second_title: Aspose.Words для .NET
description: Aspose.Words.Fields.FieldEnd сорт. Представляет конец поля Word в документе на С#.
type: docs
weight: 1860
url: /ru/net/aspose.words.fields/fieldend/
---
## FieldEnd class

Представляет конец поля Word в документе.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) статья документации.

```csharp
public class FieldEnd : FieldChar
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, которому принадлежит этот узел. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Возвращает тип поля. |
| [Font](../../aspose.words/inline/font/) { get; } | Предоставляет доступ к форматированию шрифта этого объекта. |
| [HasSeparator](../../aspose.words.fields/fieldend/hasseparator/) { get; } | Возвращает`истинный`если в этом поле есть разделитель. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Возвращает`истинный` если этот узел может содержать другие узлы. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неправильным (устаревшим) из-за других изменений , внесенных в документ. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Получает или задает, заблокировано ли родительское поле (не следует пересчитывать его результат). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Возвращает`истинный` если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Возвращает`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.fields/fieldend/nodetype/) { get; } | ВозвращаетFieldEnd . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Получает родительский элемент[`Paragraph`](../../aspose.words/paragraph/) этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../../aspose.words/range/) объект, представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldend/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | Возвращает поле для поля char. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Получает специальный символ, который представляет этот узел. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя от родителя. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

`FieldEnd` является узлом встроенного уровня и представлен [`FieldEndChar`](../../aspose.words/controlchar/fieldendchar/) управляющий символ в документе.

`FieldEnd` может быть только ребенком[`Paragraph`](../../aspose.words/paragraph/).

Полное поле в документе Microsoft Word представляет собой сложную структуру, состоящую из начального символа поля, кода поля, символа разделителя полей, поля result и конечного символа поля. Некоторые поля имеют только начало поля, код поля и конец поля.

Чтобы легко вставить новое поле в документ, используйте команду[`InsertField`](../../aspose.words/documentbuilder/insertfield/) метод.

## Примеры

Показывает, как работать с коллекцией полей.

```csharp
public void FieldCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");
    doc.UpdateFields();

    FieldCollection fields = doc.Range.Fields;

    Assert.AreEqual(6, fields.Count);

    // Перебираем коллекцию полей, выводим содержимое и печатаем
    // каждого поля с использованием пользовательской реализации посетителя.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());
}

/// <summary>
/// Реализация посетителя документа, который печатает информацию о поле.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Получает открытый текст документа, накопленный посетителем.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldStart.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldSeparator.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldEnd.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Смотрите также

* class [FieldChar](../fieldchar/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
