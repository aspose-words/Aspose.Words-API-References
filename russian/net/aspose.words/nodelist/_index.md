---
title: NodeList Class
linktitle: NodeList
articleTitle: NodeList
second_title: Aspose.Words для .NET
description: Aspose.Words.NodeList сорт. Представляет коллекцию узлов соответствующих запросу XPath выполненному с использованиемSelectNodes метод на С#.
type: docs
weight: 4220
url: /ru/net/aspose.words/nodelist/
---
## NodeList class

Представляет коллекцию узлов, соответствующих запросу XPath, выполненному с использованием[`SelectNodes`](../compositenode/selectnodes/) метод.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) статья документации.

```csharp
public class NodeList : IEnumerable<Node>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodelist/count/) { get; } | Получает количество узлов в списке. |
| [Item](../../aspose.words/nodelist/item/) { get; } | Извлекает узел по заданному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | Обеспечивает простую итерацию стиля foreach по коллекции узлов. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | Копирует все узлы из коллекции в новый массив узлов. |

## Примечания

`NodeList` возвращается[`SelectNodes`](../compositenode/selectnodes/) и содержит коллекцию узлов, соответствующих запросу XPath.

`NodeList` поддерживает индексированный доступ и итерацию.

относиться к`NodeList` Коллекция как коллекция «снимков».`NodeList`начинается как «живая» коллекция, поскольку узлы фактически не извлекаются при выполнении запроса XPath. Узлы извлекаются только при доступе, и в это время узел и все узлы, которые предшествуют ему, кэшируются, образуя коллекцию «снимков».

## Примеры

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

            // Гиперссылки в документах Word — это поля. Чтобы начать поиск гиперссылок, мы должны сначала найти все поля.
            // Используйте метод SelectNodes, чтобы найти все поля в документе через XPath.
            NodeList fieldStarts = doc.SelectNodes("//FieldStart");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // Гиперссылки, ведущие на закладки, не имеют URL-адресов.
                    if (hyperlink.IsLocal)
                        continue;

                    // Даем каждой URL-гиперссылке новый URL-адрес и имя.
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
     ///Эта реализация будет работать, только если код и имя гиперссылки состоят только из одного узла Run.
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

            // Находим узел разделителя полей.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // Обычно мы всегда можем найти конечный узел поля, но пример документа
             // содержит разрыв абзаца внутри гиперссылки, что ставит конец поля
            // в следующем абзаце. Гораздо сложнее будет обрабатывать поля, охватывающие несколько
            // абзацы правильно. В этом случае достаточно разрешить, чтобы конец поля был нулевым.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // Код поля выглядит примерно так: «ГИПЕРССЫЛКА «http:\\www.myurl.com»», но может состоять из нескольких прогонов.
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
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                 // Отображаемое имя гиперссылки сохраняется в поле результата, которое представляет собой строку «Выполнить».
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
            get => mTarget;
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
            get => mIsLocal; 
            set
            {
                mIsLocal = value;
                UpdateFieldCode();
            }
        }

        private void UpdateFieldCode()
        {
            // Код поля поля находится в узле Run между начальным узлом поля и разделителем полей.
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
            "\\S+" + // Одно или несколько ГИПЕРССЫЛОК без пробелов или другое слово на других языках.
            "\\s+" + // Один или несколько пробелов.
            "(?:\"\"\\s+)?" + // Незахватывающий необязательный "" и один или несколько пробелов.
            "(\\\\l\\s+)?" + // Необязательный флаг \l, за которым следует один или несколько пробелов.
            "\"" +  // Один апостроф.
            "([^\"]+)" + // Один или несколько символов, исключая апостроф (цель гиперссылки).
            "\"" // Один закрывающий апостроф.
        );
    }
}
```

### Смотрите также

* class [Node](../node/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
