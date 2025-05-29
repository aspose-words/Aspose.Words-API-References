---
title: StyleCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: Aspose.Words لـ .NET
description: انسخ الأنماط بسهولة باستخدام طريقة StyleCollection AddCopy. حسّن سير عمل تصميمك وبسّط إدارة أنماطك اليوم!
type: docs
weight: 70
url: /ar/net/aspose.words/stylecollection/addcopy/
---
## StyleCollection.AddCopy method

نسخ نمط إلى هذه المجموعة.

```csharp
public Style AddCopy(Style style)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| style | Style | النمط الذي سيتم نسخه. |

### قيمة الإرجاع

تم نسخ النمط جاهزًا للاستخدام.

## ملاحظات

يمكن أن ينتمي النمط المراد نسخه إلى نفس المستند أو إلى مستند مختلف.

تم نسخ النمط المرتبط.

هذه الطريقة لا تقوم بنسخ الأنماط الأساسية.

إذا كانت المجموعة تحتوي بالفعل على نمط بنفس الاسم، فسيتم إنشاء الاسم الجديد تلقائيًا عن طريق إضافة لاحقة "_number" تبدأ من 0، على سبيل المثال "Normal_0"، "Heading 1_1" وما إلى ذلك. استخدام [`Name`](../../style/name/) مُعَدِّل لتغيير اسم النمط المستورد.

## أمثلة

يوضح كيفية استيراد نمط من مستند واحد إلى مستند مختلف.

```csharp
Document srcDoc = new Document();

// إنشاء نمط مخصص للمستند المصدر.
Style srcStyle = srcDoc.Styles.Add(StyleType.Paragraph, "MyStyle");
srcStyle.Font.Color = Color.Red;

// استيراد النمط المخصص للمستند المصدر إلى المستند الوجهة.
Document dstDoc = new Document();
Style newStyle = dstDoc.Styles.AddCopy(srcStyle);

//يبدو أن النمط المستورد مطابق لمظهر نمط المصدر.
Assert.AreEqual("MyStyle", newStyle.Name);
Assert.AreEqual(Color.Red.ToArgb(), newStyle.Font.Color.ToArgb());
```

يوضح كيفية استنساخ نمط المستند.

```csharp
Document doc = new Document();

// تقوم طريقة AddCopy بإنشاء نسخة من النمط المحدد و
// يتم إنشاء اسم جديد للنمط تلقائيًا، مثل "Heading 1_0".
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

//استخدم خاصية "الاسم" الخاصة بالنمط لتغيير الاسم الذي يميز النمط.
newStyle.Name = "My Heading 1";

// تحتوي مستندنا الآن على نمطين متطابقين في المظهر ولكن بأسماء مختلفة.
// تغيير إعدادات أحد الأنماط لا يؤثر على الآخر.
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### أنظر أيضا

* class [Style](../../style/)
* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
