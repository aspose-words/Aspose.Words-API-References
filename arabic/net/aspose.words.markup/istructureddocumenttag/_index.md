---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words لـ .NET
description: استكشف واجهة Aspose.Words.Markup.IStructuredDocumentTag لإدارة علامات المستندات المنظمة بكفاءة وتعزيز معالجة المستندات الخاصة بك اليوم!
type: docs
weight: 4660
url: /ar/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

واجهة لتحديد بيانات مشتركة لـ[`StructuredDocumentTag`](../structureddocumenttag/) و[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Appearance](../../aspose.words.markup/istructureddocumenttag/appearance/) { get; set; } | يحصل على مظهر علامة المستند المنظم أو يعينه. |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | يحصل على لون علامة المستند المنظم أو يعينه. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | يحدد معرفًا رقميًا فريدًا للقراءة فقط لهذا**SDT**. |
| [IsMultiSection](../../aspose.words.markup/istructureddocumenttag/ismultisection/) { get; } | يعود صحيحًا إذا كانت هذه المثيل عبارة عن علامة مستند منظمة (متعددة الأقسام). |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | يحدد ما إذا كان محتوى هذا**SDT** يجب تفسيره بحيث يحتوي على نص نائب (على عكس محتويات النص العادي داخل SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | يحصل على المستوى الذي يتم فيه هذا**SDT** يحدث في شجرة المستندات. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | عند تعيينها على true، ستمنع هذه الخاصية المستخدم من حذف هذا**SDT** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | عند تعيينها على true، ستمنع هذه الخاصية المستخدم من تحرير محتويات هذه**SDT** . |
| [Node](../../aspose.words.markup/istructureddocumenttag/node/) { get; } | يعيد كائن العقدة الذي ينفذ هذه الواجهة. |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | يحصل على[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) يحتوي على نص نائب يجب عرضه عندما تكون محتويات تشغيل SDT هذه فارغة، عنصر XML المرتبط فارغًا كما هو محدد عبر[`XmlMapping`](./xmlmapping/) element أو[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) العنصر صحيح. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | يحصل على اسم أو تعيينه[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) يحتوي على نص نائب. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | يحصل على نوع من هذا**علامة المستند المنظم** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | يحدد علامة مرتبطة بعقدة SDT الحالية. لا يمكن أن تكون فارغة. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | يحدد الاسم الودي المرتبط بهذا**SDT** . لا يمكن أن يكون فارغًا. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | يحصل على سلسلة تمثل XML الموجود داخل العقدة فيFlatOpc تنسيق. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | يحصل على كائن يمثل تعيين علامة المستند المنظم هذه إلى XML data في جزء XML مخصص من المستند الحالي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetChildNodes](../../aspose.words.markup/istructureddocumenttag/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | يعيد مجموعة حية من العقد الفرعية التي تطابق الأنواع المحددة. |
| [RemoveSelfOnly](../../aspose.words.markup/istructureddocumenttag/removeselfonly/)() | يزيل عقدة SDT هذه فقط، لكنه يحتفظ بمحتوياتها داخل شجرة المستندات. |

## أمثلة

يوضح كيفية إزالة علامة المستند المنظمة، لكنه يحتفظ بالمحتوى بداخله.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // توفر هذه المجموعة واجهة موحدة للوصول إلى العلامات المنظمة المحددة وغير المحددة.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// هنا يمكننا الحصول على العقد الفرعية من الواجهة المشتركة للعلامات المنظمة المحددة وغير المحددة.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
