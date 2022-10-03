---
title: NodeList
second_title: Aspose.Words لمراجع .NET API
description: يمثل مجموعة من العقد المطابقة لاستعلام XPath المنفذ باستخدام امتدادSelectNodes./compositenode/selectnodes/ طريقة .
type: docs
weight: 3980
url: /ar/net/aspose.words/nodelist/
---
## NodeList class

يمثل مجموعة من العقد المطابقة لاستعلام XPath المنفذ باستخدام امتداد[`SelectNodes`](../compositenode/selectnodes/) طريقة .

```csharp
public class NodeList : IEnumerable<Node>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodelist/count/) { get; } | الحصول على عدد العقد في القائمة. |
| [Item](../../aspose.words/nodelist/item/) { get; } | استرداد عقدة في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | يوفر تكرارًا بسيطًا لنمط "foreach" عبر مجموعة العقد. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | ينسخ كل العقد من المجموعة إلى مصفوفة جديدة من العقد. |

### ملاحظات

**NodeList** تم إرجاعه بواسطة[`SelectNodes`](../compositenode/selectnodes/) ويحتوي على collection من العقد المطابقة لاستعلام XPath.

**NodeList** يدعم الوصول المفهرس والتكرار.

تعامل مع **NodeList** المجموعة كمجموعة "لقطة". **NodeList**start كمجموعة "مباشرة" لأنه لا يتم استرداد العقد فعليًا عند تشغيل استعلام XPath. يتم استرداد العقد فقط عند الوصول وفي هذا الوقت يتم تخزين العقدة وجميع العقد التي تسبقها مؤقتًا لتشكيل مجموعة "لقطة".

### أمثلة

يوضح كيفية البحث عن جميع الارتباطات التشعبية في مستند Word ، ثم تغيير عناوين URL وأسماء العرض الخاصة بهم.

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

            // الارتباطات التشعبية في مستندات Word هي حقول. لبدء البحث عن الارتباطات التشعبية ، يجب أن نجد أولاً جميع الحقول.
            // استخدم طريقة "SelectNodes" للعثور على جميع الحقول في المستند عبر XPath.
            NodeList fieldStarts = doc.SelectNodes("// FieldStart ") ;

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    // الارتباطات التشعبية التي ترتبط بالإشارات المرجعية لا تحتوي على عناوين URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // امنح كل رابط تشعبي عنوان URL واسمًا جديدين.
                    hyperlink.Target = NewUrl;
                    hyperlink.Name = NewName;
                }
            }

            doc.Save(ArtifactsDir + "ReplaceHyperlinks.Fields.docx");
        }

        private const string NewUrl = @"http://www.aspose.com ";
        private const string NewName = "Aspose - The .NET & Java Component Publisher";
    }

    /// <summary>
    /// تحتوي حقول HYPERLINK على ارتباطات تشعبية وتعرضها في نص المستند. حقل في Aspose.Words 
    /// يتكون من عدة عقد ، وقد يكون من الصعب العمل مع كل هذه العقد مباشرة. 
    /// لن يعمل هذا التنفيذ إلا إذا كان رمز الارتباط التشعبي والاسم يتكونان من عقدة تشغيل واحدة فقط.
    ///
    /// تكون بنية العقدة للحقول كما يلي:
    /// 
    /// [FieldStart] [تشغيل - رمز الحقل] [FieldSeparator] [تشغيل - نتيجة الحقل] [FieldEnd]
    /// 
    /// فيما يلي مثالان على أكواد الحقول في حقول HYPERLINK:
    /// HYPERLINK "url"
    /// HYPERLINK \ l "اسم الإشارة المرجعية"
    /// 
    /// تحتوي خاصية "النتيجة" الخاصة بالحقل على النص الذي يعرضه الحقل في نص المستند للمستخدم.
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

            // ابحث عن عقدة فاصل المجال.
            mFieldSeparator = FindNextSibling(mFieldStart, NodeType.FieldSeparator);
            if (mFieldSeparator == null)
                throw new InvalidOperationException("Cannot find field separator.");

            // في العادة ، يمكننا دائمًا العثور على عقدة نهاية الحقل ، ولكن نموذج المستند 
            // يحتوي على فاصل فقرة داخل ارتباط تشعبي ، مما يضع نهاية الحقل 
            // في الفقرة التالية. سيكون الأمر أكثر تعقيدًا للتعامل مع الحقول التي تمتد على عدة مجالات 
            // الفقرات بشكل صحيح. في هذه الحالة ، يكفي السماح بأن تكون نهاية الحقل خالية.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // يبدو رمز الحقل شيئًا مثل "HYPERLINK" http: \\ www.myurl.com "" ، ولكن يمكن أن يتكون من عدة عمليات تشغيل.
            string fieldCode = GetTextSameParent(mFieldStart.NextSibling, mFieldSeparator);
            Match match = gRegex.Match(fieldCode.Trim());

            // يكون الارتباط التشعبي محليًا إذا كان \ l موجودًا في رمز الحقل.
            mIsLocal = match.Groups[1].Length > 0; 
            mTarget = match.Groups[2].Value;
        }

        /// <summary>
        /// الحصول على أو تحديد اسم عرض الارتباط التشعبي.
        /// </summary>
        internal string Name
        {
            get => GetTextSameParent(mFieldSeparator, mFieldEnd); 
            set
            {
                // يتم تخزين اسم عرض الارتباط التشعبي في نتيجة الحقل ، وهي عبارة عن تشغيل 
                // عقدة بين فاصل المجال ونهاية الحقل.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // إذا كانت نتيجة الحقل تتكون من أكثر من تشغيل واحد ، فاحذف هذه العمليات.
                RemoveSameParent(fieldResult.NextSibling, mFieldEnd);
            }
        }

        /// <summary>
        /// الحصول على أو تحديد عنوان URL الهدف أو اسم الإشارة المرجعية للارتباط التشعبي.
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
        /// True إذا كان هدف الارتباطات التشعبية عبارة عن إشارة مرجعية داخل المستند. خطأ إذا كان الارتباط التشعبي عبارة عن عنوان URL.
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
            // يوجد رمز حقل الحقل في عقدة تشغيل بين عقدة بدء الحقل وفاصل الحقل.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // إذا كان رمز الحقل يتكون من أكثر من تشغيل واحد ، فاحذف هذه العمليات.
            RemoveSameParent(fieldCode.NextSibling, mFieldSeparator);
        }

        /// <summary>
        /// يمر عبر الأشقاء بدءًا من عقدة البداية حتى يجد عقدة من النوع المحدد أو عقدة خالية.
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
        /// يسترجع النص من البداية حتى لا يشمل عقدة النهاية.
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
        /// يزيل العقد من البداية حتى العقدة النهائية دون تضمينها.
        /// يفترض أن عقد البداية والنهاية لها نفس الأصل.
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
            "\\S+" + // واحد أو أكثر بدون مسافة HYPERLINK أو كلمة أخرى بلغات أخرى.
            "\\s+" + // مسافة واحدة أو أكثر.
            "(?:\"\"\\s+)?" + // عدم الالتقاط اختياري "" ومسافة واحدة أو أكثر.
            "(\\\\l\\s+)?" + // اختياري \ l علامة متبوعة بمسافة واحدة أو أكثر.
            "\"" + // فاصلة عليا واحدة.    
            "([^\"]+)" + // حرف أو أكثر ، باستثناء الفاصلة العليا (هدف الارتباط التشعبي).
            "\"" // فاصلة عليا واحدة للإغلاق.
        );
    }
}
```

### أنظر أيضا

* class [Node](../node/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
