---
title: Class FieldStart
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldStart فصل. يمثل بداية حقل Word في مستند.
type: docs
weight: 2280
url: /ar/net/aspose.words.fields/fieldstart/
---
## FieldStart class

يمثل بداية حقل Word في مستند.

```csharp
public class FieldStart : FieldChar
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص . |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة . |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata/) { get; } | الحصول على بيانات الحقل المخصصة المرتبطة بالحقل. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | إرجاع نوع الحقل. |
| [Font](../../aspose.words/inline/font/) { get; } | يوفر الوصول إلى تنسيق خط هذا الكائن. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع صحيح إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | إرجاع صحيح إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | الحصول على أو تحديد ما إذا كان الحقل الأصلي مغلقًا (يجب عدم إعادة حساب النتيجة) . |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | عوائد **حقيقي** إذا تم نقل (حذف) هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | عوائد **حقيقي** إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغيير. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype/) { get; } | عوائدFieldStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | الحصول على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | استرداد الأصل[`Paragraph`](../../aspose.words/paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ **نطاق** الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept/)(DocumentVisitor) | يقبل الزائر . |
| [Clone](../../aspose.words/node/clone/)(bool) | لإنشاء نسخة مكررة من العقدة . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | يحصل على أول سلف محدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | الحصول على الأصل الأول لنوع الكائن المحدد. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | إرجاع حقل للحقل char . |
| override [GetText](../../aspose.words/specialchar/gettext/)() | يحصل على الحرف الخاص الذي تمثله هذه العقدة . |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز الشجرة بالطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | يصدر محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

### ملاحظات

`FieldStart` هي عقدة ذات مستوى مضمن ويتم تمثيلها بواسطة [`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar/) حرف التحكم في المستند.

`FieldStart` يمكن أن يكون فقط تابعًا لـ[`Paragraph`](../../aspose.words/paragraph/).

الحقل الكامل في مستند Microsoft Word عبارة عن بنية معقدة تتكون من حرف بداية الحقل ، ورمز الحقل ، وحرف فاصل الحقل ، ونتائج الحقل وحرف نهاية الحقل. تحتوي بعض الحقول فقط على بداية الحقل ورمز الحقل ونهاية الحقل.

لإدراج حقل جديد بسهولة في مستند ، استخدم ملحق[`InsertField`](../../aspose.words/documentbuilder/insertfield/) طريقة .

### أمثلة

يوضح كيفية العمل مع مجموعة من الحقول.

```csharp
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

    // تكرار عبر المجموعة الميدانية ، وطباعة المحتويات والنوع
    // من كل حقل باستخدام تنفيذ زائر مخصص.
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

/// <summary>
/// تنفيذ الزائر المستند الذي يطبع معلومات الحقل.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// يحصل على النص العادي للمستند الذي قام الزائر بتجميعه.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة FieldStart في المستند.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة FieldSeparator في المستند.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة FieldEnd في المستند.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

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

* class [FieldChar](../fieldchar/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


