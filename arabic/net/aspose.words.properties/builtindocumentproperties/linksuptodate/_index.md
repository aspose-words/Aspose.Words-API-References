---
title: BuiltInDocumentProperties.LinksUpToDate
linktitle: LinksUpToDate
articleTitle: LinksUpToDate
second_title: Aspose.Words لـ .NET
description: اكتشف ميزة BuiltInDocumentProperties LinksUpToDate، مما يضمن تحديث الروابط التشعبية في مستندك ويعزز موثوقية المحتوى الخاص بك.
type: docs
weight: 200
url: /ar/net/aspose.words.properties/builtindocumentproperties/linksuptodate/
---
## BuiltInDocumentProperties.LinksUpToDate property

يشير إلى ما إذا كانت الارتباطات التشعبية في المستند محدثة.

```csharp
public bool LinksUpToDate { get; set; }
```

## ملاحظات

لا يقوم Aspose.Words بتحديث هذه الخاصية.

## أمثلة

يوضح كيفية العمل مع خصائص المستند في فئة "المحتوى".

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // باستخدام الخصائص المضمنة،
    // يمكننا التعامل مع إحصائيات المستند مثل عدد الكلمات/الصفحات/الأحرف كبيانات وصفية يمكن الاطلاع عليها دون فتح المستند
    // يمكن الوصول إلى هذه الخصائص عن طريق النقر بزر الماوس الأيمن فوق الملف في مستكشف Windows والانتقال إلى الخصائص > التفاصيل > المحتوى
    // إذا أردنا عرض هذه البيانات داخل المستند، فيمكننا استخدام حقول مثل NUMPAGES وNUMWORDS وNUMCHARS وما إلى ذلك.
    // كما يمكن أيضًا عرض هذه القيم في Microsoft Word من خلال التنقل عبر ملف > خصائص > خصائص متقدمة > إحصائيات
    // عدد الصفحات: تعرض خاصية PageCount عدد الصفحات في الوقت الفعلي ويمكن تعيين قيمتها لخاصية Pages

     //تخزن خاصية "الصفحات" عدد صفحات المستند.
    Assert.AreEqual(6, properties.Pages);

    // تعرض الخصائص المضمنة "الكلمات" و"الأحرف" و"الأحرف ذات المسافات" أيضًا إحصائيات مختلفة للمستند،
    // ولكننا نحتاج إلى استدعاء طريقة "UpdateWordCount" على المستند بأكمله قبل أن نتوقع أن يحتوي على قيم دقيقة.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // احسب عدد الأسطر في المستند، ثم قم بتعيين النتيجة إلى الخاصية المضمنة "الأسطر".
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // تعيين عدد عقد الفقرات في المستند إلى الخاصية المضمنة "الفقرات".
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // احصل على تقدير لحجم ملف مستندنا عبر الخاصية المضمنة "Bytes".
    Assert.AreEqual(20310, properties.Bytes);

    // قم بتعيين قالب مختلف لمستندنا، ثم قم بتحديث خاصية "القالب" المضمنة يدويًا لتعكس هذا التغيير.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);

    properties.Template = doc.AttachedTemplate;

    //"ContentStatus" هي خاصية مضمنة وصفية.
    properties.ContentStatus = "Draft";

    // عند الحفظ، ستحتوي الخاصية المضمنة "ContentType" على نوع MIME لتنسيق الحفظ الناتج.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // إذا كانت الوثيقة تحتوي على روابط، وكانت جميعها محدثة، فيمكننا تعيين الخاصية "LinksUpToDate" إلى "true".
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// يحسب عدد الأسطر في المستند.
/// يجتاز شجرة كيانات تخطيط المستند أثناء الإنشاء،
/// حساب الكيانات من نوع "السطر" التي تحتوي أيضًا على نص حقيقي.
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
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
