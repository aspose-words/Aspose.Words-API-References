---
title: BuiltInDocumentProperties.Bytes
second_title: Aspose.Words لمراجع .NET API
description: BuiltInDocumentProperties ملكية. يمثل تقديرًا لعدد البايتات في المستند.
type: docs
weight: 20
url: /ar/net/aspose.words.properties/builtindocumentproperties/bytes/
---
## BuiltInDocumentProperties.Bytes property

يمثل تقديرًا لعدد البايتات في المستند.

```csharp
public int Bytes { get; set; }
```

### ملاحظات

لا يقوم Microsoft Word دائمًا بتعيين هذه الخاصية.

لا يقوم Aspose.Words بتحديث هذه الخاصية.

### أمثلة

يوضح كيفية العمل مع خصائص المستند في فئة "المحتوى".

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // باستخدام الخصائص المضمنة،
    // يمكننا التعامل مع إحصائيات المستند مثل عدد الكلمات/الصفحة/الأحرف كبيانات وصفية يمكن إلقاء نظرة سريعة عليها دون فتح المستند
    // يتم الوصول إلى هذه الخصائص عن طريق النقر بزر الماوس الأيمن على الملف في مستكشف Windows والانتقال إلى الخصائص > التفاصيل > محتوى
    // إذا أردنا عرض هذه البيانات داخل المستند، فيمكننا استخدام حقول مثل NUMPAGES وNUMWORDS وNUMCHARS وما إلى ذلك.
    // يمكن أيضًا عرض هذه القيم في برنامج Microsoft Word من خلال التنقل في الملف > الخصائص > خصائص متقدمة > إحصائيات
    // عدد الصفحات: تعرض خاصية PageCount عدد الصفحات في الوقت الفعلي ويمكن تعيين قيمتها لخاصية الصفحات

     // تقوم خاصية "الصفحات" بتخزين عدد صفحات المستند.
    Assert.AreEqual(6, properties.Pages);

    // تعرض الخصائص المضمنة "Words" و"Characters" و"CharactersWithSpaces" أيضًا إحصائيات مستند متنوعة،
    // ولكننا نحتاج إلى استدعاء أسلوب "UpdateWordCount" في المستند بأكمله قبل أن نتوقع احتوائه على قيم دقيقة.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // احسب عدد الأسطر في المستند، ثم قم بتعيين النتيجة إلى خاصية "الأسطر" المضمنة.
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // قم بتعيين عدد عقد الفقرة في المستند إلى خاصية "الفقرات" المضمنة.
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // احصل على تقدير لحجم ملف وثيقتنا عبر خاصية "البايت" المضمنة.
    Assert.AreEqual(20310, properties.Bytes);

    // قم بتعيين قالب مختلف للمستند الخاص بنا، ثم قم بتحديث خاصية "القالب" المضمنة يدويًا لتعكس هذا التغيير.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);    

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus" هي خاصية وصفية مدمجة.
    properties.ContentStatus = "Draft";

    // عند الحفظ، ستحتوي الخاصية المضمنة "ContentType" على نوع MIME لتنسيق حفظ الإخراج.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // إذا كانت الوثيقة تحتوي على روابط، وجميعها محدثة، فيمكننا ضبط خاصية "LinksUpToDate" على "صحيح".
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// يحسب الأسطر في المستند.
/// يجتاز شجرة كيانات تخطيط المستند عند الإنشاء،
/// كيانات العد من النوع "الخط" التي تحتوي أيضًا على نص حقيقي.
/// </summary>
private class LineCounter
{
    public LineCounter(Document doc)
    {
        mLayoutEnumerator = new LayoutEnumerator(doc);

        CountLines();
    }

    public int GetLineCount()
    {
        return mLineCount;
    }

    private void CountLines()
    {
        do
        {
            if (mLayoutEnumerator.Type == LayoutEntityType.Line)
            {
                mScanningLineForRealText = true;
            }

            if (mLayoutEnumerator.MoveFirstChild())
            {
                if (mScanningLineForRealText && mLayoutEnumerator.Kind.StartsWith("TEXT"))
                {
                    mLineCount++;
                    mScanningLineForRealText = false;
                }
                CountLines();
                mLayoutEnumerator.MoveParent();
            }
        } while (mLayoutEnumerator.MoveNext());
    }

    private readonly LayoutEnumerator mLayoutEnumerator;
    private int mLineCount;
    private bool mScanningLineForRealText;
}
```

### أنظر أيضا

* class [BuiltInDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../builtindocumentproperties/)
* المجسم [Aspose.Words](../../../)


