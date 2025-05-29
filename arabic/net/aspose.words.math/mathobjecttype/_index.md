---
title: MathObjectType Enum
linktitle: MathObjectType
articleTitle: MathObjectType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Math.MathObjectType enum لتحديد أنواع كائنات Office Math وإدارتها بسهولة لتحسين معالجة المستندات.
type: docs
weight: 4800
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
| OMath | `0` | مثال للنص الرياضي. |
| OMathPara | `1` | فقرة رياضية، أو منطقة عرض رياضية، تحتوي على فقرة رياضية واحدة أو أكثرOMath العناصر الموجودة في وضع العرض. |
| Accent | `2` | دالة التشكيل، تتكون من قاعدة وعلامة تشكيلية مركبة. |
| Bar | `3` | دالة Bar، تتكون من وسيطة أساسية وشريط علوي أو شريط سفلي. |
| BorderBox | `4` | كائن Border Box، يتكون من حدود مرسومة حول مثيل من النص الرياضي (مثل الصيغة أو المعادلة) |
| Box | `5` | كائن مربع، يستخدم لتجميع مكونات معادلة أو مثيل آخر للنص الرياضي. |
| Delimiter | `6` | كائن فاصل يتكون من فواصل فتح وإغلاق (مثل الأقواس، وأقواس ، والأقواس المربعة، والأشرطة الرأسية)، وعنصر موجود بداخله. |
| Degree | `7` | درجة في الجذر الرياضي. |
| Argument | `8` | كائن وسيطة . يُغلِق كيانات Office Math عند استخدامها كوسائط لكيانات Office Math أخرى. |
| Array | `9` | كائن مصفوفة يتكون من معادلة واحدة أو أكثر أو تعبير أو نص رياضي آخر يعمل ويمكن محاذاته رأسياً كوحدة بالنسبة للنص المحيط على السطر. |
| Fraction | `10` | كائن كسري، يتكون من بسط ومقام مفصولين بشريط كسري. |
| Denominator | `11` | مقام الكسر. |
| Numerator | `12` | بسط كائن الكسر. |
| Function | `13` | كائن تطبيق الوظيفة، والذي يتكون من اسم الوظيفة وعنصر الحجة الذي تم التصرف عليه. |
| FunctionName | `14` | اسم الدالة. على سبيل المثال، أسماء الدوال هي: sin وcos. |
| GroupCharacter | `15` | كائن مجموعة الأحرف، يتكون من حرف مرسوم أعلى أو أسفل النص، غالبًا بغرض تجميع العناصر بصريًا |
| Limit | `16` | الحد الأدنى لـLowerLimit الكائن و الحد الأعلى لـUpperLimit دالة. |
| LowerLimit | `17` | كائن الحد الأدنى، يتكون من نص على خط الأساس ونص بحجم مخفض أسفله مباشرة. |
| UpperLimit | `18` | كائن الحد الأعلى، يتكون من نص على خط الأساس ونص بحجم مخفض أعلى منه مباشرة. |
| Matrix | `19` | كائن مصفوفة يتكون من عنصر واحد أو أكثر موزعة في صف واحد أو أكثر وعمود واحد أو أكثر. |
| MatrixRow | `20` | صف واحد من المصفوفة. |
| NAry | `21` | كائن N-ary، يتكون من كائن N-ary، وقاعدة (أو متغير)، وحدود علوية وسفلية اختيارية. |
| Phantom | `22` | كائن شبحي. |
| Radical | `23` | كائن جذري، يتكون من جذر وعنصر أساسي ودرجة اختيارية . |
| SubscriptPart | `24` | مؤشر الكائن الذي يمكن أن يحتوي على جزء مؤشر. |
| SuperscriptPart | `25` | أعلى الكائن العلوي. |
| PreSubSuperscript | `26` | كائن ما قبل النص العلوي الفرعي، والذي يتكون من عنصر أساسي ونص سفلي ونص علوي موضوعين على يسار القاعدة. |
| Subscript | `27` | كائن فرعي، يتكون من عنصر أساسي ونص برمجي بحجم مخفض موضوع أسفله وإلى اليمين. |
| SubSuperscript | `28` | كائن علوي فرعي، يتكون من عنصر أساسي، ونص مخفض الحجم موضوع أسفله وإلى اليمين، ونص مخفض الحجم موضوع أعلىه وإلى اليمين. |
| Supercript | `29` | كائن علوي، يتكون من عنصر أساسي ونص بحجم مخفض موضوع أعلى وإلى اليمين. |

## أمثلة

يوضح كيفية طباعة بنية العقدة لكل عقدة رياضيات مكتبية في مستند.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // عندما نحصل على عقدة مركبة لقبول زائر مستند، يقوم الزائر بزيارة العقدة المستقبلة،
    // ثم يمر عبر جميع أبناء العقدة بطريقة العمق أولاً.
    //يمكن للزائر قراءة وتعديل كل عقدة تمت زيارتها.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يجتاز شجرة العقد غير الثنائية المكونة من عقد فرعية.
/// إنشاء خريطة في شكل سلسلة من جميع عقد OfficeMath التي تمت مواجهتها وأطفالها.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// يحصل على النص العادي للمستند الذي جمعه الزائر.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة تشغيل في المستند.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عند مواجهة عقدة OfficeMath في المستند.
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
    /// أضف سطرًا إلى StringBuilder وقم بتدويره وفقًا لمدى عمق الزائر في شجرة المستند.
    /// </summary>
    /// <اسم المعلمة="نص"></param>
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
