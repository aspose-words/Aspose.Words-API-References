---
title: MathObjectType
second_title: Aspose.Words لمراجع .NET API
description: يحدد نوع كائن Office الرياضي .
type: docs
weight: 3870
url: /ar/net/aspose.words.math/mathobjecttype/
---
## MathObjectType enumeration

يحدد نوع كائن Office الرياضي .

```csharp
public enum MathObjectType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| OMath | `0` | مثيل النص الرياضي . |
| OMathPara | `1` | فقرة رياضية ، أو عرض منطقة رياضية ، تحتوي على واحد أو أكثرOMath العناصر الموجودة في وضع العرض. |
| Accent | `2` | دالة تشكيل ، تتكون من قاعدة وعلامة تشكيل مجمعة . |
| Bar | `3` | دالة شريطية ، تتكون من وسيطة أساسية وشريط علوي أو شريط سفلي. |
| BorderBox | `4` | كائن مربع الحدود ، يتكون من حد مرسوم حول مثيل نص رياضي (مثل صيغة أو معادلة) |
| Box | `5` | كائن Box ، الذي يُستخدم لتجميع مكونات معادلة أو مثيل آخر للنص الرياضي. |
| Delimiter | `6` | كائن محدد ، يتكون من محددات الفتح والإغلاق (مثل الأقواس والأقواس والأقواس والأشرطة الرأسية) ، وعنصر مضمن بالداخل. |
| Degree | `7` | درجة في الجذر الرياضي . |
| Argument | `8` | كائن وسيطة. إحاطة كيانات Office Math عند استخدامها كوسيطات لكيانات Office Math الأخرى. |
| Array | `9` | كائن صفيف يتكون من معادلة واحدة أو أكثر أو تعبيرات أو نص رياضي آخر يعمل يمكن ضبطه رأسياً كوحدة فيما يتعلق بالنص المحيط على السطر . |
| Fraction | `10` | كائن كسر يتكون من بسط ومقام مفصولين بشريط كسر . |
| Denominator | `11` | مقام كائن كسر . |
| Numerator | `12` | بسط كائن الكسر . |
| Function | `13` | كائن تطبيق الوظيفة ، والذي يتكون من اسم دالة وعنصر وسيطة يتم التعامل معه. |
| FunctionName | `14` | اسم الوظيفة. على سبيل المثال ، أسماء الوظائف هي sin و cos. |
| GroupCharacter | `15` | كائن مجموعة الأحرف ، يتكون من حرف مرسوم أعلى أو أسفل النص ، غالبًا بغرض تجميع العناصر بشكل مرئي |
| Limit | `16` | الحد الأدنى لملفLowerLimit الكائن و الحد الأعلى لملفUpperLimit الوظيفة. _ |
| LowerLimit | `17` | كائن ذو حد أدنى ، يتكون من نص على خط الأساس ونص بحجم أصغر أسفله مباشرةً. |
| UpperLimit | `18` | كائن ذو حد أعلى ، يتكون من نص في الخط الأساسي ونص بحجم أصغر فوقه مباشرةً . |
| Matrix | `19` | عنصر مصفوفة يتكون من عنصر واحد أو أكثر تم وضعه في صف واحد أو أكثر وعمود واحد أو أكثر. |
| MatrixRow | `20` | صف واحد من المصفوفة . |
| NAry | `21` | كائن N-ary ، يتكون من كائن n-ary وقاعدة (أو معامل) وحدود علوية وسفلية اختيارية. |
| Phantom | `22` | كائن فانتوم . |
| Radical | `23` | كائن جذري يتكون من جذري وعنصر أساسي ودرجة اختيارية . |
| SubscriptPart | `24` | نص منخفض للكائن الذي يمكن أن يحتوي على جزء منخفض. |
| SuperscriptPart | `25` | نص مرتفع للكائن المرتفع . |
| PreSubSuperscript | `26` | كائن Pre-Sub-Superscript ، والذي يتكون من عنصر أساسي وخط منخفض ومرتفع موضوع على يسار القاعدة . |
| Subscript | `27` | كائن منخفض ، يتكون من عنصر أساسي ونص صغير الحجم موضوع أسفل وإلى اليمين . |
| SubSuperscript | `28` | كائن فرعي مرتفع ، يتكون من عنصر أساسي ، نص برمجي صغير الحجم موضوع أسفل وإلى اليمين ، ونص برمجي صغير الحجم موضوع أعلى وإلى اليمين . |
| Supercript | `29` | كائن مرتفع ، يتكون من عنصر أساسي ونص صغير الحجم يتم وضعه في الأعلى وإلى اليمين . |

### أمثلة

يوضح كيفية طباعة بنية العقدة لكل عقدة رياضية للمكتب في مستند.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر المستند ، يزور الزائر عقدة القبول ،
    // ثم يعبر جميع أبناء العقدة بطريقة العمق أولاً.
    // يمكن للزائر قراءة كل عقدة تمت زيارتها وتعديلها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يتجاوز الشجرة غير الثنائية للعقد الفرعية للعقد.
/// ينشئ خريطة في شكل سلسلة لجميع عقد OfficeMath التي تمت مواجهتها وأطفالها.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// يحصل على النص العادي للمستند الذي قام الزائر بتجميعه.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// يتم الاستدعاء عند مواجهة عقدة تشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاستدعاء عند مصادفة عقدة OfficeMath في المستند.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها بعد زيارة جميع العقد الفرعية لعقدة OfficeMath.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// قم بإلحاق سطر بـ StringBuilder وقم بعمل مسافة بادئة له اعتمادًا على مدى عمق الزائر في شجرة المستند.
    /// </summary>
    /// < param name = "text" > < / param >
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideOfficeMath;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Math](../../aspose.words.math/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
