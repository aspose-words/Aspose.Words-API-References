---
title: FieldStart Class
linktitle: FieldStart
articleTitle: FieldStart
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldStart, ваш ключ к эффективному управлению полями Word в документах. Улучшите обработку документов сегодня!
type: docs
weight: 2840
url: /ru/net/aspose.words.fields/fieldstart/
---
## FieldStart class

Представляет начало поля Word в документе.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldStart : FieldChar
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata/) { get; } | Получает данные пользовательского поля, связанные с полем. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Возвращает тип поля. |
| [Font](../../aspose.words/inline/font/) { get; } | Предоставляет доступ к форматированию шрифта этого объекта. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Возврат`истинный` если этот узел может содержать другие узлы. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Возвращает значение true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений , внесенных в документ. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Возвращает значение true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Возвращает значение true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Возвращает или задает, заблокировано ли родительское поле (не следует пересчитывать его результат). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Возврат`истинный` если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Возврат`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype/) { get; } | ВозвратFieldStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Возвращает родителя[`Paragraph`](../../aspose.words/paragraph/) этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../../aspose.words/range/)объект, представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | Возвращает поле для поля char. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Получает специальный символ, который представляет этот узел. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

`FieldStart` является узлом встроенного уровня и представлен как the [`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar/) управляющий символ в документе.

`FieldStart` может быть только ребенком[`Paragraph`](../../aspose.words/paragraph/).

Полное поле в документе Microsoft Word представляет собой сложную структуру, состоящую из символа начала поля, кода поля, символа разделителя полей, результата поля и символа конца поля. Некоторые поля имеют только начало поля, код поля и конец поля.

Чтобы легко вставить новое поле в документ, используйте[`InsertField`](../../aspose.words/documentbuilder/insertfield/) Метод .

## Примеры

Показывает, как работать с набором полей.

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

    // Проходим по коллекции полей и выводим содержимое и тип
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
/// Реализация посетителя документа, который выводит информацию о поле.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Получает простой текст документа, накопленный посетителем.
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

Показывает, как найти все гиперссылки в документе Word, а затем изменить их URL-адреса и отображаемые имена.

```csharp
using System;
using System.Linq;
using System.Text;
using System.Text.RegularExpressions;
using Aspose.Words;
using Aspose.Words.Fields;
using NUnit.Framework;

namespace ApiExamples
{
    public class ExReplaceHyperlinks : ApiExampleBase
    {
        public void Fields()
        {
            Document doc = new Document(MyDir + "Hyperlinks.docx");

            // Гиперссылки в документах Word — это поля. Чтобы начать искать гиперссылки, мы должны сначала найти все поля.
            // Используйте метод «SelectNodes» для поиска всех полей в документе с помощью XPath.
            NodeList fieldStarts = doc.SelectNodes("//FieldStart");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // Гиперссылки, ведущие на закладки, не имеют URL-адресов.
                    if (hyperlink.IsLocal)
                        continue;

                    // Дайте каждой гиперссылке URL новый URL и имя.
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http://www.aspose.com";
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

     ///<summary>
      ///Поля HYPERLINK содержат и отображают гиперссылки в теле документа. Поле в Aspose.Words
      ///состоит из нескольких узлов, и может быть сложно работать со всеми этими узлами напрямую.
     ///Эта реализация будет работать только в том случае, если код и имя гиперссылки состоят только из одного узла Run.
    ///
     ///Структура узла для полей следующая:
     ///
     ///[FieldStart][Run - field code][FieldSeparator][Run - field result][FieldEnd]
     ///
     ///Below are two example field codes of HYPERLINK fields:
     ///HYPERLINK "url"
     ///HYPERLINK \l "bookmark name"
     ///
     ///A field's "Result" property contains text that the field displays in the document body to the user.
     ///</summary>
    internal class Hyperlink
    {
        internal Hyperlink(FieldStart fieldStart)
        {
            if (fieldStart == null)
                throw new ArgumentNullException("fieldStart");
            if (fieldStart.FieldType != FieldType.FieldHyperlink)
                throw new ArgumentException("Field start type must be FieldHyperlink.");

            mFieldStart = fieldStart;

            // Найти узел разделителя полей.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // Обычно мы всегда можем найти конечный узел поля, но в примере документа
             // содержит разрыв абзаца внутри гиперссылки, что переводит поле в конец
             // в следующем абзаце. Будет гораздо сложнее обрабатывать поля, которые охватывают несколько
            // абзацы правильно. В этом случае достаточно разрешить полю end быть null.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Код поля выглядит примерно так: «HYPERLINK "http:\\www.myurl.com"», но может состоять из нескольких строк.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // Гиперссылка является локальной, если в коде поля присутствует \l.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

         ///<summary>
         ///Gets or sets the display name of the hyperlink.
         ///</summary>
        internal string Name
        {
            get
            {
                return GetTextSameParent(mFieldSeparator, mFieldEnd);
            }
            set
            {
                 // Отображаемое имя гиперссылки сохраняется в поле result, которое является Run
                // узел между разделителем полей и концом поля.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // Если результат поля состоит из более чем одного прогона, удалите эти прогоны.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

         ///<summary>
         ///Gets or sets the target URL or bookmark name of the hyperlink.
         ///</summary>
        internal string Target
        {
            get
            {
                return mTarget;
            }
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

         ///<summary>
         ///True if the hyperlinks target is a bookmark inside the document. False if the hyperlink is a URL.
         ///</summary>
        internal bool IsLocal
        {
            get
            {
                return mIsLocal;
            }
            set
            {
                mIsLocal = value;
                UpdateFieldCode();
            }
        }

        private void UpdateFieldCode()
        {
            // Код поля находится в узле Run между начальным узлом поля и разделителем полей.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // Если код поля состоит из более чем одного прогона, удалите эти прогоны.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

         ///<summary>
         ///Goes through siblings starting from the start node until it finds a node of the specified type or null.
         ///</summary>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

         ///<summary>
         ///Retrieves text from start up to but not including the end node.
         ///</summary>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

         ///<summary>
         ///Removes nodes from start up to but not including the end node.
         ///Assumes that the start and end nodes have the same parent.
         ///</summary>
        private static void RemoveSameParent(Node startNode, Node endNode)
        {
            if (endNode != null && startNode.ParentNode != endNode.ParentNode)
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            Node curChild = startNode;
            while ((curChild != null) && (curChild != endNode))
            {
                Node nextChild = curChild.NextSibling;
                curChild.Remove();
                curChild = nextChild;
            }
        }

        private readonly Node mFieldStart;
        private readonly Node mFieldSeparator;
        private readonly Node mFieldEnd;
        private bool mIsLocal;
        private string mTarget;

        private static readonly Regex gRegex = new Regex(
            "\\S+" + // Одна или несколько ГИПЕРССЫЛОК без пробелов или других слов на других языках.
            "\\s+" + // Один или несколько пробелов.
            "(?:\"\"\\s+)?" + // Необязательный незахватывающий символ "" и один или несколько пробелов.
            "(\\\\l\\s+)?" + // Необязательный флаг \l, за которым следует один или несколько пробелов.
            "\"" +  // Один апостроф.
            "([^\"]+)" + // Один или несколько символов, за исключением апострофа (цель гиперссылки).
            "\"" // Один закрывающий апостроф.
        );
    }
}
```

### Смотрите также

* class [FieldChar](../fieldchar/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
