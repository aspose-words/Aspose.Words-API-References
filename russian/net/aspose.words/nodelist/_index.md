---
title: NodeList
second_title: Справочник по API Aspose.Words для .NET
description: Представляет набор узлов соответствующих запросу XPath выполненному с использованием методаSelectNodes./compositenode/selectnodes.
type: docs
weight: 3930
url: /ru/net/aspose.words/nodelist/
---
## NodeList class

Представляет набор узлов, соответствующих запросу XPath, выполненному с использованием метода[`SelectNodes`](../compositenode/selectnodes).

```csharp
public class NodeList : IEnumerable<Node>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodelist/count) { get; } | Получает количество узлов в списке. |
| [Item](../../aspose.words/nodelist/item) { get; } | Извлекает узел по заданному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator)() | Обеспечивает простую итерацию в стиле foreach по набору узлов. |
| [ToArray](../../aspose.words/nodelist/toarray)() | Копирует все узлы из коллекции в новый массив узлов. |

### Примечания

**NodeList** возвращается by[`SelectNodes`](../compositenode/selectnodes)и содержит коллекцию узлов, соответствующих запросу XPath.

**NodeList** поддерживает индексированный доступ и итерацию.

Рассматривать коллекцию **NodeList** как коллекцию "моментальных снимков". **NodeList** запускается как "живая" коллекция, поскольку узлы фактически не извлекаются при выполнении запроса XPath. Узлы извлекаются только при доступе, и в это время узел и все предшествующие ему узлы кэшируются, образуя коллекцию "моментальных снимков".

### Примеры

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

             // Гиперссылки в документах Word являются полями. Чтобы начать поиск гиперссылок, мы должны сначала найти все поля.
             // Используйте метод "SelectNodes", чтобы найти все поля в документе через XPath.
            NodeList fieldStarts = doc.SelectNodes(" //Начало поля");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                     // Гиперссылки на закладки не имеют URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // Дайте каждой гиперссылке URL новый URL и имя.
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http: //www.aspose.com";
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

    /// <summary>
     /// Поля HYPERLINK содержат и отображают гиперссылки в теле документа. Поле в Aspose.Words 
     /// состоит из нескольких узлов, и работать со всеми этими узлами напрямую может быть сложно. 
     /// Эта реализация будет работать, только если код и имя гиперссылки состоят только из одного узла Run.
     ///
     /// Структура узла для полей следующая:
       /// 
     /// [FieldStart][Выполнить - код поля][FieldSeparator][Выполнить - результат поля][FieldEnd]
       /// 
     /// Ниже приведены два примера кодов полей ГИПЕРССЫЛКИ: 
     /// ГИПЕРССЫЛКА "url"
     /// ГИПЕРССЫЛКА \l "имя закладки"
       /// 
     /// Свойство «Результат» поля содержит текст, который поле отображает в теле документа для пользователя.
    /// </summary>
    internal class Hyperlink
    {
        internal Hyperlink(FieldStart fieldStart)
        {
            if (fieldStart == null)
                throw new ArgumentNullException("fieldStart");
            if (fieldStart.FieldType != FieldType.FieldHyperlink)
                throw new ArgumentException("Field start type must be FieldHyperlink.");

            mFieldStart = fieldStart;

             // Находим узел-разделитель полей.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

            // Обычно мы всегда можем найти конечный узел поля, но пример документа 
             // содержит разрыв абзаца внутри гиперссылки, что ставит конец поля 
             // в следующем абзаце. Будет намного сложнее обрабатывать поля, которые охватывают несколько 
             // абзацы правильно. В этом случае достаточно, чтобы конец поля был нулевым.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

             // Код поля выглядит примерно так: "ГИПЕРССЫЛКА "http:\\www.myurl.com"", но может состоять из нескольких прогонов.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

             // Гиперссылка является локальной, если в поле code.
 присутствует \l
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

        /// <summary>
         /// Получает или задает отображаемое имя гиперссылки.
        /// </summary>
        internal string Name
        {
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                 // Отображаемое имя гиперссылки хранится в поле результата, которое представляет собой Run 
                 // узел между разделителем полей и концом поля.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                 // Если результат поля состоит из более чем одного прогона, удаляем эти прогоны.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

        /// <summary>
         /// Получает или устанавливает целевой URL или имя закладки гиперссылки.
        /// </summary>
        internal string Target
        {
            get => mTarget;
            set
            {
                mTarget = value;
                UpdateFieldCode();
            }
        }

        /// <summary>
        /// Истинно, если целью гиперссылки является закладка внутри документа. False, если гиперссылка является URL-адресом.
        /// </summary>
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

             // Если код поля состоит из нескольких прогонов, удалить эти прогоны.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

        /// <summary>
         /// Просматривает братьев и сестер, начиная с начального узла, пока не найдет узел указанного типа или null.
        /// </summary>
        private static Node FindNextSibling(Node startNode, NodeType nodeType)
        {
            for (Node node = startNode; node != null; node = node.NextSibling)
            {
                if (node.NodeType == nodeType)
                    return node;
            }

            return null;
        }

        /// <summary>
         /// Получает текст от начала до конечного узла, но не включая его.
        /// </summary>
        private static string GetTextSameParent(Node startNode, Node endNode)
        {
            if ((endNode != null) && (startNode.ParentNode != endNode.ParentNode))
                throw new ArgumentException("Start and end nodes are expected to have the same parent.");

            StringBuilder builder = new StringBuilder();
            for (Node child = startNode; !child.Equals(endNode); child = child.NextSibling)
                builder.Append(child.GetText());

            return builder.ToString();
        }

        /// <summary>
         /// Удаляет узлы от начального до конечного узла, но не включая его.
         /// Предполагается, что начальный и конечный узлы имеют одного и того же родителя.
        /// </summary>
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
            "\\S+" +  // Одна или несколько ГИПЕРССЫЛОК без пробелов или других слов на других языках.
            "\\s+" +  // Один или несколько пробелов.
            "(?:\"\"\\s+)?" +  // Незахватывающий необязательный "" и один или несколько пробелов.
            "(\\\\l\\s+)?" +  // Необязательный флаг \l, за которым следует один или несколько пробелов.
            "\"" +  // Один апостроф. 
            "([^\"]+)" + // Один или несколько символов, кроме апострофа (цель гиперссылки).
            "\""  // Один закрывающий апостроф.
        );
    }
}
```

### Смотрите также

* class [Node](../node)
* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
