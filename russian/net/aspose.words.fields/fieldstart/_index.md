---
title: FieldStart
second_title: Справочник по API Aspose.Words для .NET
description: Представляет начало поля Word в документе.
type: docs
weight: 2240
url: /ru/net/aspose.words.fields/fieldstart/
---
## FieldStart class

Представляет начало поля Word в документе.

```csharp
public class FieldStart : FieldChar
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| virtual [Document](../../aspose.words/node/document) { get; } | Получает документ, которому принадлежит данный узел. |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata) { get; } | Получает данные пользовательского поля, связанные с полем. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype) { get; } | Возвращает тип поля. |
| [Font](../../aspose.words/inline/font) { get; } | Предоставляет доступ к форматированию шрифта этого объекта. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Возвращает true, если этот узел может содержать другие узлы. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неправильным (устаревшим) из-за других изменений , внесенных в документ. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked) { get; set; } | Получает или устанавливает, заблокировано ли родительское поле (не должно пересчитывать его результат). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | Возвращает **true** , если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | Возвращает **true** , если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype) { get; } | ВозвращаетFieldStart. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | Извлекает родителя[`Paragraph`](../../aspose.words/paragraph)этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает объект **Range** , представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept)(DocumentVisitor) | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| [GetField](../../aspose.words.fields/fieldchar/getfield)() | Возвращает поле для поля char. |
| override [GetText](../../aspose.words/specialchar/gettext)() | Получает специальный символ, который представляет этот узел. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove)() | Удаляет себя из родителя. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

[`FieldStart`](../fieldstart)является узел встроенного уровня и представлен управляющим символом [`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar)в документе.

[`FieldStart`](../fieldstart)может быть только потомкомПараграф.

Полное поле в документе Microsoft Word представляет собой сложную структуру, состоящую из начального символа поля, кода поля, символа-разделителя поля, поля результат и символ конца поля. Некоторые поля имеют только начало поля, код поля и конец поля.

Чтобы легко вставить новое поле в документ, используйте[`InsertField`](../../aspose.words/documentbuilder/insertfield) метод.

### Примеры

Показывает, как работать с коллекцией полей.

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

* class [FieldChar](../fieldchar)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
