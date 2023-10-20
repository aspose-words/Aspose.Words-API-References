---
title: FieldStart Class
linktitle: FieldStart
articleTitle: FieldStart
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.FieldStart فصل. يمثل بداية حقل Word في المستند في C#.
type: docs
weight: 2430
url: /ar/net/aspose.words.fields/fieldstart/
---
## FieldStart class

يمثل بداية حقل Word في المستند.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldStart : FieldChar
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| [FieldData](../../aspose.words.fields/fieldstart/fielddata/) { get; } | يحصل على بيانات الحقل المخصصة المرتبطة بالحقل. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | إرجاع نوع الحقل. |
| [Font](../../aspose.words/inline/font/) { get; } | يوفر الوصول إلى تنسيق الخط لهذا الكائن. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | إرجاع صحيح إذا تم حذف هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | إرجاع صحيح إذا تم تغيير تنسيق الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | إرجاع صحيح إذا تم إدراج هذا الكائن في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل الأصلي مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (حذفه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | إرجاع`حقيقي` إذا تم نقل هذا الكائن (إدراجه) في Microsoft Word أثناء تمكين تعقب التغييرات. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| override [NodeType](../../aspose.words.fields/fieldstart/nodetype/) { get; } | إرجاعFieldStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | يسترد الأصل[`Paragraph`](../../aspose.words/paragraph/) من هذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../../aspose.words/range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldstart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | يقبل الزائر. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | إنشاء نسخة مكررة من العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | يحصل على السلف الأول للمحدد[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | الحصول على السلف الأول لنوع الكائن المحدد. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | إرجاع حقل للحقل char. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | الحصول على الحرف الخاص الذي تمثله هذه العقدة. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |

## ملاحظات

`FieldStart` هي عقدة على المستوى المضمّن ويتم تمثيلها بواسطة [`FieldStartChar`](../../aspose.words/controlchar/fieldstartchar/) حرف التحكم في المستند.

`FieldStart` لا يمكن إلا أن يكون طفلا[`Paragraph`](../../aspose.words/paragraph/).

الحقل الكامل في مستند Microsoft Word عبارة عن بنية معقدة تتكون من حرف بداية الحقل ورمز الحقل وحرف فاصل الحقل ونتيجة الحقل وحرف نهاية الحقل. تحتوي بعض الحقول فقط على بداية الحقل ورمز الحقل ونهاية الحقل.

لإدراج حقل جديد في مستند بسهولة، استخدم[`InsertField`](../../aspose.words/documentbuilder/insertfield/) طريقة .

## أمثلة

يوضح كيفية العمل مع مجموعة من الحقول.

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

    // كرر المجموعة الميدانية واطبع المحتويات واكتبها
    // لكل حقل باستخدام تطبيق زائر مخصص.
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
/// تنفيذ مستند الزائر الذي يطبع معلومات الحقل.
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
    /// يتم الاتصال به عند مواجهة عقدة FieldStart في المستند.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة FieldSeparator في المستند.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة FieldEnd في المستند.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

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

* class [FieldChar](../fieldchar/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
