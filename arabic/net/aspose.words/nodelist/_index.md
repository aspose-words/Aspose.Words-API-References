---
title: NodeList Class
linktitle: NodeList
articleTitle: NodeList
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.NodeList، الحل الأمثل لإدارة نتائج استعلامات XPath بكفاءة وتحسين قدرات معالجة المستندات.
type: docs
weight: 4910
url: /ar/net/aspose.words/nodelist/
---
## NodeList class

يمثل مجموعة من العقد المطابقة لاستعلام XPath الذي تم تنفيذه باستخدام[`SelectNodes`](../compositenode/selectnodes/) الطريقة.

لمعرفة المزيد، قم بزيارة[نموذج كائن المستند (DOM) في Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class NodeList : IEnumerable<Node>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodelist/count/) { get; } | يحصل على عدد العقد في القائمة. |
| [Item](../../aspose.words/nodelist/item/) { get; } | يسترجع عقدة عند الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words/nodelist/getenumerator/)() | يوفر تكرارًا بسيطًا بأسلوب "foreach" عبر مجموعة العقد. |
| [ToArray](../../aspose.words/nodelist/toarray/)() | نسخ جميع العقد من المجموعة إلى مجموعة جديدة من العقد. |

## ملاحظات

`NodeList` يتم إرجاعه بواسطة[`SelectNodes`](../compositenode/selectnodes/) ويحتوي على مجموعة من العقد المطابقة لاستعلام XPath.

`NodeList` يدعم الوصول المفهرس والتكرار.

علاج`NodeList` المجموعة كمجموعة "لقطة".`NodeList` يبدأ كمجموعة "حية" لأن العقد لا يتم استردادها فعليًا عند تشغيل استعلام XPath. يتم استرداد العقد فقط عند الوصول وفي هذا الوقت يتم تخزين العقدة وكل العقد التي تسبقها مؤقتًا لتشكيل مجموعة "لقطة".

## أمثلة

يوضح كيفية العثور على جميع الارتباطات التشعبية في مستند Word، ثم تغيير عناوين URL وأسماء العرض الخاصة بها.

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

            // الروابط التشعبية في مستندات Word هي حقول. للبدء بالبحث عن الروابط التشعبية، يجب أولاً العثور على جميع الحقول.
            //استخدم طريقة "SelectNodes" للعثور على جميع الحقول في المستند عبر XPath.
            NodeList fieldStarts = doc.SelectNodes("//بدء الحقل");

            foreach (FieldStart fieldStart in fieldStarts.OfType<FieldStart>())
            {
                if (fieldStart.FieldType == FieldType.FieldHyperlink)
                {
                    Hyperlink hyperlink = new Hyperlink(fieldStart);

                    //الروابط التشعبية التي ترتبط بالإشارات المرجعية لا تحتوي على عناوين URL.
                    if (hyperlink.IsLocal)
                        continue;

                    // أعط كل رابط تشعبي لـ URL عنوان URL جديدًا واسمًا.
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
      ///تحتوي حقول الارتباط التشعبي على روابط تشعبية وتعرضها في نص المستند. حقل في Aspose.Words
      ///يتكون من عدة عقد، وقد يكون من الصعب العمل مع كل هذه العقد بشكل مباشر.
     ///سيعمل هذا التنفيذ فقط إذا كان كود الارتباط التشعبي واسم كل منهما يتكون من عقدة تشغيل واحدة فقط.
    ///
     ///هيكل العقدة للحقول هو كما يلي:
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

             // عادةً، يمكننا دائمًا العثور على عقدة نهاية الحقل، ولكن مستند المثال
             // يحتوي على فاصل فقرة داخل ارتباط تشعبي، مما يضع نهاية الحقل
             // في الفقرة التالية. سيكون التعامل مع الحقول التي تمتد على عدة
            // الفقرات بشكل صحيح. في هذه الحالة، يكفي أن تكون نهاية الحقل فارغة.
            mFieldEnd = FindNextSibling(mFieldSeparator, NodeType.FieldEnd);

            // يبدو رمز الحقل مثل "HYPERLINK "http:\\www.myurl.com""، ولكنه قد يتكون من عدة عمليات تشغيل.
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
            get
            {
                return GetTextSameParent(mFieldSeparator, mFieldEnd);
            }
            set
            {
                 // يتم تخزين اسم عرض الارتباط التشعبي في حقل النتيجة، وهو عبارة عن تشغيل
                //عقدة بين فاصل الحقل ونهاية الحقل.
                Run fieldResult = (Run) mFieldSeparator.NextSibling;
                fieldResult.Text = value;

                // إذا كانت نتيجة الحقل تتكون من أكثر من تشغيل واحد، فاحذف هذه التشغيلات.
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
            // يوجد رمز حقل الحقل في عقدة التشغيل بين عقدة بداية الحقل وفاصل الحقل.
            Run fieldCode = (Run) mFieldStart.NextSibling;
            fieldCode.Text = string.Format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget);

            // إذا كان رمز الحقل يتكون من أكثر من تشغيل واحد، فاحذف هذه التشغيلات.
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
            "\\S+" + // كلمة واحدة أو أكثر بدون مسافات HYPERLINK أو كلمة أخرى في لغات أخرى.
            "\\s+" + // مسافة واحدة أو أكثر.
            "(?:\"\"\\s+)?" + // اختياري غير قابل للالتقاط "" ومسافة واحدة أو أكثر.
            "(\\\\l\\s+)?" + // علامة اختيارية \l متبوعة بمسافة واحدة أو أكثر.
            "\"" +  //علامة اقتباس واحدة.
            "([^\"]+)" + // حرف واحد أو أكثر، باستثناء علامة الاقتباس العليا (هدف الارتباط التشعبي).
            "\"" //علامة ختامية واحدة.
        );
    }
}
```

### أنظر أيضا

* class [Node](../node/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
