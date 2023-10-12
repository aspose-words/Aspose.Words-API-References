---
title: Enum MathObjectType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Math.MathObjectType تعداد. يحدد نوع كائن Office Math.
type: docs
weight: 4110
url: /ar/net/aspose.words.math/mathobjecttype/
---
## MathObjectType enumeration

يحدد نوع كائن Office Math.

```csharp
public enum MathObjectType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| OMath | `0` | مثيل النص الرياضي. |
| OMathPara | `1` | فقرة الرياضيات، أو عرض منطقة الرياضيات، التي تحتوي على واحدة أو أكثرOMath العناصر الموجودة في وضع العرض. |
| Accent | `2` | دالة التشكيل، وتتكون من قاعدة وعلامة تشكيل مجمعة. |
| Bar | `3` | دالة شريطية، تتكون من وسيطة أساسية وشريط علوي أو شريط سفلي. |
| BorderBox | `4` | كائن Border Box، الذي يتكون من حد مرسوم حول مثيل نص رياضي (مثل صيغة أو معادلة) |
| Box | `5` | كائن Box، الذي يُستخدم لتجميع مكونات المعادلة أو مثيل آخر للنص الرياضي. |
| Delimiter | `6` | كائن محدد، يتكون من محددات الفتح والإغلاق (مثل الأقواس، الأقواس، والأقواس، والأشرطة العمودية)، وعنصر موجود بداخلها. |
| Degree | `7` | الدرجة في الجذر الرياضي. |
| Argument | `8` | كائن الوسيطة. يقوم بتضمين كيانات Office Math عند استخدامها كوسيطات لكيانات Office Math الأخرى. |
| Array | `9` | كائن مصفوفة، يتكون من واحدة أو أكثر من المعادلات أو التعبيرات أو أي نص رياضي آخر يعمل والذي يمكن ضبطه رأسيًا كوحدة فيما يتعلق بالنص المحيط على السطر. |
| Fraction | `10` | كائن الكسر، يتكون من البسط والمقام مفصولين بشريط كسر. |
| Denominator | `11` | مقام كائن الكسر. |
| Numerator | `12` | بسط كائن الكسر. |
| Function | `13` | كائن تطبيق الوظيفة، والذي يتكون من اسم دالة وعنصر وسيطة يتم التصرف بناءً عليه. |
| FunctionName | `14` | اسم الدالة. على سبيل المثال، أسماء الوظائف هي sin وcos. |
| GroupCharacter | `15` | كائن مجموعة الأحرف، يتكون من حرف مرسوم أعلى النص أو أسفله، غالبًا بغرض تجميع العناصر بشكل مرئي |
| Limit | `16` | الحد الأدنى للLowerLimit الكائن و الحد الأعلى للUpperLimit الوظيفة. |
| LowerLimit | `17` | كائن ذو حد أدنى، يتكون من نص على الخط الأساسي ونص صغير الحجم أسفله مباشرة. |
| UpperLimit | `18` | كائن ذو حد علوي، يتكون من نص على الخط الأساسي ونص صغير الحجم فوقه مباشرة. |
| Matrix | `19` | كائن مصفوفة، يتكون من عنصر واحد أو أكثر موضوعة في صف واحد أو أكثر وعمود واحد أو أكثر. |
| MatrixRow | `20` | صف واحد من المصفوفة. |
| NAry | `21` | كائن N-ary، يتكون من كائن n-ary، وقاعدة (أو معامل)، وحدود عليا ودنيا اختيارية. |
| Phantom | `22` | الكائن الوهمي. |
| Radical | `23` | كائن جذري يتكون من عنصر جذري وعنصر أساسي ودرجة اختيارية . |
| SubscriptPart | `24` | منخفض للكائن الذي يمكن أن يحتوي على جزء منخفض. |
| SuperscriptPart | `25` | مرتفع للكائن المرتفع. |
| PreSubSuperscript | `26` | كائن Pre-Sub-Superscript، والذي يتكون من عنصر أساسي ومنخفض ومرتفع يقع على يسار القاعدة. |
| Subscript | `27` | كائن منخفض، يتكون من عنصر أساسي وبرنامج نصي صغير الحجم موضوع في الأسفل وعلى اليمين. |
| SubSuperscript | `28` | كائن مرتفع فرعي، يتكون من عنصر أساسي، وبرنامج نصي صغير الحجم موضوع بالأسفل وإلى اليمين، وبرنامج نصي صغير الحجم موضوع بالأعلى وإلى اليمين. |
| Supercript | `29` | كائن مرتفع، يتكون من عنصر أساسي وبرنامج نصي صغير الحجم موضوع في الأعلى وعلى اليمين. |

### أمثلة

يوضح كيفية طباعة بنية العقدة لكل عقدة رياضية في المكتب في المستند.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر المستند، يقوم الزائر بزيارة العقدة المقبولة،
    // ثم يجتاز جميع أبناء العقدة بطريقة العمق الأول.
    // يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يجتاز الشجرة غير الثنائية للعقدة التابعة.
/// ينشئ خريطة على شكل سلسلة لجميع عقد OfficeMath التي تمت مواجهتها وأبناءها.
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
    /// يتم الاتصال به عند مواجهة عقدة التشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عند مواجهة عقدة OfficeMath في المستند.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به بعد زيارة كافة العقد التابعة لعقدة OfficeMath.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// ألحق سطرًا بـ StringBuilder وقم بوضع مسافة بادئة له اعتمادًا على مدى عمق الزائر في شجرة المستندات.
    /// </summary>
    /// <param name="text"></param>
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


