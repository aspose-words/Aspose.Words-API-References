---
title: Class NodeList
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.NodeList فصل. يمثل مجموعة من العقد المطابقة لاستعلام XPath الذي تم تنفيذه باستخدامSelectNodes الطريقة.
type: docs
weight: 4220
url: /ar/net/aspose.words/nodelist/
---
## NodeList class

يمثل مجموعة من العقد المطابقة لاستعلام XPath الذي تم تنفيذه باستخدام[`SelectNodes`](../compositenode/selectnodes/) الطريقة.

لمعرفة المزيد، قم بزيارة[نموذج كائن مستند Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class NodeList : IEnumerable<Node>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodelist/count/) { get; } | الحصول على عدد العقد في القائمة. |
| [Item](../../aspose.words/nodelist/item/) { get; } | يسترد عقدة في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | يوفر تكرارًا بسيطًا لنمط "foreach" عبر مجموعة العقد. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | نسخ كافة العقد من المجموعة إلى مجموعة جديدة من العقد. |

### ملاحظات

`NodeList` يتم إرجاعها بواسطة[`SelectNodes`](../compositenode/selectnodes/) ويحتوي على مجموعة من العقد المطابقة لاستعلام XPath.

`NodeList` يدعم الوصول المفهرسة والتكرار.

علاج`NodeList` المجموعة كمجموعة "لقطة".`NodeList`يبدأ كمجموعة "مباشرة" لأنه لا يتم استرداد العقد فعليًا عند تشغيل استعلام XPath. يتم استرداد العقد فقط عند الوصول وفي هذا الوقت يتم تخزين العقدة وجميع العقد التي تسبق مؤقتًا لتشكل مجموعة "لقطة".

### أمثلة

يوضح كيفية البحث عن كافة الارتباطات التشعبية في مستند Word، ثم تغيير عناوين URL وأسماء العرض الخاصة بها.

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

            // الارتباطات التشعبية في مستندات Word هي حقول. للبدء في البحث عن الارتباطات التشعبية، يجب علينا أولاً العثور على كافة الحقول.
            // استخدم طريقة "SelectNodes" للعثور على كافة الحقول في المستند عبر XPath.
            NodeList fieldStarts = doc.SelectNodes("//فيلدستارت");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // الارتباطات التشعبية التي ترتبط بالإشارات المرجعية لا تحتوي على عناوين URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // أعط كل رابط تشعبي لعنوان URL عنوان URL واسمًا جديدًا.
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
      ///تحتوي حقول الارتباط التشعبي على الارتباطات التشعبية وتعرضها في نص المستند. حقل في Aspose.Words
      ///يتكون من عدة عقد، وقد يكون من الصعب العمل مع كل تلك العقد مباشرة.
     ///لن يعمل هذا التنفيذ إلا إذا كان كل من رمز الارتباط التشعبي واسمه يتكونان من عقدة تشغيل واحدة فقط.
    ///
     ///بنية العقدة للحقول هي كما يلي:
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

            // ابحث عن عقدة فاصل الحقل.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

             // عادةً، يمكننا دائمًا العثور على عقدة نهاية الحقل، ولكن المستند النموذجي
             // يحتوي على فاصل فقرة داخل الارتباط التشعبي، مما يضع نهاية الحقل
            // في الفقرة التالية. سيكون التعامل مع الحقول التي تمتد لعدة مرات أكثر تعقيدًا
            // الفقرات بشكل صحيح. في هذه الحالة، يعد السماح لنهاية الحقل بأن تكون فارغة أمرًا كافيًا.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // يبدو رمز الحقل مثل "HYPERLINK "http:\\www.myurl.com""، ولكنه يمكن أن يتكون من عدة عمليات تشغيل.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // يكون الارتباط التشعبي محليًا إذا كان \l موجودًا في رمز الحقل.
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
                 // يتم تخزين اسم عرض الارتباط التشعبي في نتيجة الحقل، وهو تشغيل
                // العقدة بين فاصل الحقل ونهاية الحقل.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // إذا كانت نتيجة الحقل تتكون من أكثر من عملية تشغيل واحدة، فاحذف عمليات التشغيل هذه.
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
            // رمز حقل الحقل موجود في عقدة التشغيل بين عقدة بداية الحقل وفاصل الحقل.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // إذا كان رمز الحقل يتكون من أكثر من تشغيل واحد، فاحذف عمليات التشغيل هذه.
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
            "\\S+" + // واحد أو أكثر بدون مسافات HYPERLINK أو كلمة أخرى في اللغات الأخرى.
            "\\s+" + // مسافة واحدة أو أكثر.
            "(?:\"\"\\s+)?" + // عدم الالتقاط اختياري "" ومسافة واحدة أو أكثر.
            "(\\\\l\\s+)?" + // علامة \l اختيارية متبوعة بمسافة واحدة أو أكثر.
            "\"" +  // فاصلة عليا واحدة.
            "([^\"]+)" + // حرف واحد أو أكثر، باستثناء الفاصلة العليا (هدف الارتباط التشعبي).
            "\"" // فاصلة علوية واحدة للإغلاق.
        );
    }
}
```

### أنظر أيضا

* class [Node](../node/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


